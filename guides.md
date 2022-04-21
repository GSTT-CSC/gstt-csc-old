---
layout: howto
title: How-to
description: Instructions, SOPs and guides
---
<div class="card" style="width: 18rem;">
   <div class="card-body">
      <h5 class="card-title">Contents</h5>
      <ol>
      1. <a href="#ANON">XNAT anonymisation guide</a><br>
      </ol>
   </div>
</div>


<hr>


## <a name=ANON></a>**XNAT: the anonymisation guide**
`XNAT is a virtual platform capable of storing and managing medical images and associated data. Within Guy’s and St Thomas’ NHS Foundation Trust, it forms a part of the local secure enclave for the purposes of federated learning in artificial intelligence projects. The data is ingested from PACS into XNAT where it is anonymised and sorted into relevant projects, ensuring data is only visible to those who need it, and allowing for data deletion upon project completion. This guide describes the process of data collection, de-identification and data storage in XNAT and details how compliance with DICOM Supplement 142 is achieved.`
<br><br>
Medical imaging data is stored in a DICOM format. DICOM stands for *Digital Imaging and Communications in Medicine* and is an international standard format for medical image storage, retrieval, processing and transfer. DICOM images consist of the actual acquired image as a set of pixels and a DICOM header. Data coded within the DICOM header are a series of attributes describing the scan and the patient. Each attribute is tagged with a unique DICOM tag which consists of a group and element number and each tag has a name to identify the type of information (or attribute) contained within the tag. This principle of data tagging allows DICOMs to be compared, transferred, stored and queried.
<br>
<br>
Before any medical data can be used in research or for training of AI algorithms, it must first be completely de-identified such that no data used can be traced back to any individual. To do this, the DICOM tags need to be altered, deleted or manipulated in such a way that the image no longer describes the individual. Because there are many DICOM tags within a DICOM header and since what is and what is not identifiable information is not always straightforward, a DICOM Standard Supplement 142 was created, outlining best anonymisation practices for purposes of clinical trials. We adopted the same standard for our de-identification purposes.
<br>
<br>
Anonymisation in XNAT is done at 2 levels: firstly when data arrives into XNAT from PACS (site-wide anonymisation) and secondly when data are moved from the pre-archive into the assigned project (project-level anonymisation).
<br>
<h2>Data collection</h2>
Data can be ingested into XNAT via two routes: 
<ul>
<li>Pushed from PACS via Teleradiology</li>
<li>Pulled from within XNAT using query-retrieve (Q/R)</li>
</ul>
Teleradiology is used for sending individual DICOM objects to XNAT. The sender must have access to Sectra and the necessary permissions to send from Sectra to ‘GSTT_XNAT’ destination. The permissions are managed by the PACS team.
<br>
<br>
Q/R is used for importing batches of data. The data required can be manually searched by accession number, patient name, patient ID or the date range; or they can be requested by uploading a .csv file. The instructions on how to format the .csv file can be found [here](https://wiki.xnat.org/xnat-tools/dicom-query-retrieve-plugin/using-dqr-bulk-querying-and-importing-via-csv-file).
<br>
<h2>De-identification via teleradiology</h2>
Teleradiology is used to send individual DICOM objects from PACS to XNAT. As the data leave PACS, text is automatically appended to two DICOM tags: the Patient Comment Field (0010,4000) and Study Comment Field (0032,4000). The text is: 

    Project:Unassigned Subject:subj001 Session:subj001_sess001

This ensures that the patient name and accession number do not reach XNAT’s pre-archive. It instead sets the subject ID to subj001 and the session ID as subj001_sess001. This means that all data which is sent via Teleradiology from PACS will arrive in XNAT with the same subject and session ID. These are then manually changed when moving the data from pre-archive to archive by the project owner. The data in XNAT can be distinguished based on timestamp of arrival matched to the timestamp in Sectra so the project owner can tell which DICOM object belongs to which study subject. Only individual scans should be sent via this route – for batches larger than 3 to 5 scans, please use Q/R.

All other data in the DICOM headers is removed, changed or replaced as detailed in the anonymisation scripts.
<br>
<h2>De-identification via Q/R</h2>
When data is imported using Q/R functionalities of XNAT, new subject ID and session ID can be assigned to each scan imported. It's recommended a .csv is used for DQR upload, in which case the subject and session IDs can be specified in directly in the .csv.
<br>
<br>
All other data in the DICOM headers is removed, changed or replaced as detailed in the anonymisation scripts.
<br>
<h2>Data access and storage</h2>
The project owner has the reading, writing, updating and deleting rights of all data they own. They can grant access to other users to either view-only or modify the existing data. Data can also be shared between projects as read-only.
<br>
<br>
The data will be stored on physical storage kept with GSTT.
<br>
<h2>Resources</h2>
More information XNAT can be found on [their website](https://www.xnat.org/).
<br>
<br>
More information on DICOM standard Supplement 142 concerning clinical trial de-identification can be found [here](https://www.dicomstandard.org/News-dir/ftsup/docs/sups/sup142.pdf).
<br>
<br>
Below are our anonymisation scripts. Patient age, size, weight, ethnic group, smoking status and pregnancy status are retained. Manufacturer private tags are removed by this script.  The manipulation of the DICOM data follows the DICOM Standards Supplement 142, which specifies which tags should be removed, replaced, or manipulated to ensure traceability to individual from the data shared is not possible. Some UIDs which do not contain any time of date data are also retained.
<br>
<br>
[Site-wide anonymisation script](assets/XNAT_anonymisation/Site-wide anon script.txt)
<br>
<br>
[Project-level anonymisation script](assets/XNAT_anonymisation/Project-specific anon script.txt)


<hr>


## <a name=NDOO></a>**National Data Opt-Out Policy (NDOO)**
`The national data opt-out was introduced on 25 May 2018, enabling patients to opt out from the use of their data for secondary uses, i.e. any use outside of direct clinical care, such as audit and research, in line with the recommendations of the National Data Guardian in her Review of Data Security, Consent and Opt-Outs. In order to comply with this policy, staff members must use the National Data Opt-Out Check Service to check whether a patient has a recorded opt-out before processing their data. This guide describes the process of using the service, achieving policy compliance, exempt use cases, and provides more information on the policy itself. The current compliance deadline is 31 July 2022.`

The [National Data Opt-Out Check Service](https://optout.gstt.nhs.uk/#/login) is a web application which enables GSTT staff members to check whether a patient has a recorded opt-out. This service checks NHS Digital's National Opt-Out database by using their Message Exchange for Social Care and Health (MESH) and only staff members with up-to-date Information Governance training should use the service.

Before processing patient data, staff members must perform this check and submit the NHS number(s) of the patient(s) eligible for inclusion in their project. Staff members can submit one NHS number or upload a CSV file with one or up to 100,000 NHS numbers per request. The response file will be sent to the GSTT email address indicated in the request and confirms the patients who have **not** opted out. For a step-by-step walkthrough, please refer to the NDOO Check Service section in the SOPs page [here](SOPs.md#NDOOCheckService).

In order to comply with the NDOO policy, only patients contained in the response file should be retained and all patients who are **not** in the response file should be **removed** from the project.

**Please note, however, that patients may choose to opt in or out throughout the lifespan of a project and so the NDOO Check Service must be used regularly, i.e. daily or any other regular basis as approved by Information Govenrance in the project's Data Protection Impact Assessment (DPIA).**
<br>
<h2>Recording patient opt-out</h2>
Patients can view or change their national data opt-out choice at any time by either:
<ul>
<li>Using the NHS online service <a href="https://www.nhs.uk/your-nhs-data-matters">here</a></li>
<li>Clicking on "Your Health" in the NHS App (download for iOS <a href="https://apps.apple.com/gb/app/nhs-app/id1388411277">here</a> and Android <a href="https://play.google.com/store/apps/details?id=com.nhs.online.nhsonline&hl=en_GB&gl=US">here</a>), and selecting "Choose if data from your health records is shared for research and planning".</li>
</ul>
<h2>Exempt Use Cases</h2>
Existing projects that already use anonymised data are out of scope and can proceed without the NDOO check.
<br>
<h2>Resources</h2>
For more information on the policy at the trust and national level, please refer to the GTi page [here](https://gti.gstt.local/services/infogov/national-data-opt-out.aspx) and the NHS Digital page [here](https://digital.nhs.uk/services/national-data-opt-out)
<br>
<br>
For more information on NHS Digital's MESH service, please visit their page [here](https://digital.nhs.uk/services/message-exchange-for-social-care-and-health-mesh).
<br>
<br>
For any other questions about the policy and achieving compliance, please reach out to the Information Governance team on their group email address [here](mailto:askIG@gstt.nhs.uk).
