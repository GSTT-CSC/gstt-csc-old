---
layout: howto
title: How-to
description: Instructions, SOPs and guides
---

<div class="card" style="width: 18rem;">
   <div class="card-body">
      <h5 class="card-title">Contents</h5>
      <ol>
      1. <a href="#QIPS">Registering a project on QIPS</a><br>
      2. <a href="#XNATupload">Uploading data to XNAT</a><br>
      3. <a href="#CogStackSearch">Using Cogstack for data search</a>
      </ol>
   </div>
</div>


<hr>


## <a name=QIPS></a>**Register your project on QIPS**
`First, make sure that your project falls under 'service development' and not 'research' by checking http://www.hra-decisiontools.org.uk/research/. Then, make sure the clinical lead is happy to be added as a collaborator on the QIPS system. Once you're sure of both, proceed to step 1.`

All AI projects must be registered with the Trust Quality Improvement and Patient Safety Team as a service evaluation/clinical audit on the trust database on the following link: 

    http://tww-wafr/WAFR-FAD/Login.aspx?ReturnUrl=/WAFR-FAD/Applications/ClinicalAuditV2/Default.aspx 

1. Log in with your existing Trust credentials.  

2. Select ‘create new proposal’ tab. 
3. Proposal type is ‘service evaluation’ 
4. Type in the project title as agreed with radiologists 
5. Add the clinical lead as the proposer.  
6. Add your telephone number. 
7. Select ‘no’ for ‘is proposal trust wide’ 
8. For lead speciality, select ‘medical physics’ 
9. For ‘responsible person’, type in your own name 
10. For ‘reasons for carrying out this project, select ‘high risk service’, ‘of local concern’, ‘identified as a problem’ and / or ‘quality improvement’ and any other that may apply. 
11. For ‘objective’, briefly explain what we are trying to achieve with this project. 
12. Click ‘save’, then press ‘next’. 

13. For ‘stakeholder’ write ‘radiologists’, select all activities they will be involved with and press the green plus button. 
14. If the project does not involve patients or carers, select ‘no’, else select 'yes'. 
15. For population, describe who will be included, e.g. ‘all chest CT’, and who will be excluded (if any). 
16. For population or sample, select all that apply as they apply, choosing to gather data from 1/1 of last year to 31/1 of last year. Select data collection strategy (e.g. retrospective) and the data sources (e. g. patient records). 
17. Click ‘save’, then press ‘next’. 
 
18. Click on ‘add measures’. A pop-up will appear.  
19. Set the standard or acceptable level of compliance (frequently '100%' but write whatever is appropriate for your project)  
20. Describe the evidence of quality of care or service – how will we know whether the AI is working? Example evidence: ‘lung nodule in chest CT is correctly reported in report’ 
21. There are ‘no’ exception. 
22. The data collection instructions should describe how data will be acquired, e.g. ‘studies to be exported from PACS and processed ‘offline’’. 
23. Click ‘Add measures’. 
24. Fill in the target dates, e.g. for data collection (1 month from start), findings to be reviewed by 3 months from the data collection date, report to be submitted 3 months from the findings date. 
25. Click ‘save’, click ‘next’.	 

26. Select all boxes which apply. This is likely to be all boxes. 
27. Click ‘next’. 
28. Agree with the declaration by ticking the box and click on ‘next’. Click on submit. 

The proposal will be sent to the Specialty QI & Audit lead for approval and then to the Directorate QI & Audit lead. Once approved you will be notified by email. 



<hr>



## <a name=XNATupload></a>**Uploading data to XNAT**
`Before you start make yourself a cup of tea or get a snack, put on some soothing music or a podcast in the background. XNAT is slow and you will need to be patient with it else you will keep cancelling your own commands. Pop-ups can be slow and the amount of data moved takes much time. I recommend you start this at the end of the day instead of at the beginning and leave it to go over night to account for higher bandwidth demands on PACS during office hours.`

1.	Log into the GSTT network and open a browser. <br>

2.	Go to https://sp-pr-flipml01.gstt.local and log in with your username. If you do not have a username, contact Dika to make one for you.

3.	If the project doesn’t exist yet, create it:
    1.	New -> Project -> Fill in the boxes (project title, running title and project ID can be the same). Add the project description and the investigators (name and email are sufficient). Create the project. 

4.	The project page will open. On the right-hand side, choose ‘Import From PACS’.

5.	This will open the data query-retrieve (DQR) page which allows you to query Sectra PACS for the requested images. 
    <ul><li>You can use the DQR in two ways: by entering the search criteria or by importing a CSV file</li>
        <ol><li>Search criteria: you can use accession number or patient ID and date range and you can use * for wildcard. Click on ‘Search PACS’. Wait for the results to show. Once you find the correct scan(s), tick the box on the left-hand side. Then press the ‘Begin Import’ button at the bottom of the screen. A pop-up will appear to select all series which are relevant. Select all which are relevant (if you’re importing CTs, de-select the Dose Info, Dose Report and the Patient Protocol series, as they contain burnt-in patient data!). Click ‘Import’. </li>
            <li>CSV: you can upload a correctly-formatted CSV to perform a bulk search. This is described <a href=" https://wiki.xnat.org/xnat-tools/dicom-query-retrieve-plugin/using-dqr-bulk-querying-and-importing-via-CSV-file">here</a>. The CSV file should contain either your Accession Numbers (which uniquely identify a scan) or a Patient ID and a study date. If you're using the latter method, pay special attention to the formatting of the dates which should be YYYYMMDD to match the date formatting in PACS. To do the search click on ‘import CSV’ at the top of the page. Choose your CSV file. Click on ‘upload’. The query will begin – it may take a while. If an error occurs, test your CSV file by reducing it to only one query and see if that comes up with what you expect. Once you can query all you want at once without issue, you’ll have to select which scans to import. NB: XNAT can only handle about 20-30 import queries at once, else it will get stuck on retrieving series information screen. If you’re importing CTs, de-select the Dose Info, Dose Report and the Patient Protocol series, as those contain burnt-in images of dates and names. Click on ‘Import Selected’. Wait until you get a notification that the query had been sent to PACS. Then click on ‘Close’. You will need to upload the CSV again to select the next batch for import.</li>
        </ol></ul>
<br>    
6.	The imported data will appear in the pre-archive (Upload -> Go to prearchive). Click ‘Refresh’ if your data isn’t there, or check the Import Queue (Upload ->  Import Queue/History) – the data takes a while to transfer.

7.	In the pre-archive, you can review the details of your import, such as files and DICOM tags. Once you’ve confirmed you’re happy with the data, select it in the pre-archive (tick the left-hand side checkbox) and select ‘Change projects’ on the right-hand side. Select your project. This will assign the data to your project. You can then ‘Archive’ it, which will move the data from the pre-archive into your project folder.

8.	You can now view, amend and interact with the data in the project (Browse -> My Projects -> your folder). You can check the DICOM tags of each data session (click on the Subject then hover over the scan details until 3 icons appear – the first is View Details, select this to view tags), you can view the session (click on ‘View Session’ on the right-hand side). You can also delete or download the images here or in the project details. 



<hr>



## <a name=CogStackSearch></a>**Using Cogstack for data search**
`CogStack is an information and extraction platform which allows us to search the EPR (electronic patient records). It is a catalogue of hospital documents and can be used to identify patient cohorts as well as search for clinical information for other purposes (e.g. AI software evaluation). Please note that CogStack is an index of documents and not an index of patients, so many answers will be buried in the free text of each document that will need analysis. Please also note that access to CogStack needs to be requested by your line manager. There are also two levels of access: a reader and an admin. If you are granted reader access, you will be able to search CogStack but not to export any data. If you need data export, please talk to a colleague with admin access and they can help you retrieve your CSV files.`

1.	Log into the GSTT network and open a browser. <br>

2.	Go to https://cogstack.gstt.nhs.uk:5601 and select 'Log in with GSTT authentication'. You may be prompted to input your GSTT Username and Password.

3.	An Access Agreement notice will appear warning you that you are about to see sensitive information. Press the 'Acknowledge and continue' button.

4.	You wil be presented with your home dashboard. Click on the three lines (the menu) on the left-hand side of the screen, just under the 'Elastic' logo and under 'Analytics' tab select 'Discover'.

5. 	You will be then presented with a search bar (at the top), the results panel (centre right) and the index panel (centre left).

6. 	CogStack is built upon ElasticSearch and follows its query logic. Most of the fields within each document are tagged with an ID by which you can use to search through the documents, e.g. 'patient_TrustNumber'. The syntax in general is 

    keyword : "search term" AND keyword : "second search term" OR keyword : "third search term" AND NOT keyword : "exclusion term"

    You can use as many or as few keywords as you wish. You can find the keywords by either inspecting a document or by scrolling through the options that drop down when you click on the search bar. NB that 'body_analysed' means the free text area of the document - your search terms are most likely to appear there. When you are happy with your query, press the 'Enter' or click on 'Update' buttom at the end of the search bar.

7.  The results panel will populate with documents that match your search terms. If your search is very broad, this may take a few seconds. An error box will appear on the bottom right corner if there are errors with the search term itself. To investigate your results, click on the arrow on the left-hand side of each search result to expand it.

8.	The index selected as the default is e&#42;. Different indexes are catalogues of different documents. For most of our purposes, you will want to access either gstt_clinical_documents_letters or gstt_clinical_epr&#42;. The latter contains observations, orders and results and will contain things such as blood test orders and results, pathology results, and radiology reports. The former will contain the letters sent to patient's primary care clinician (usually GP or whoever referred them for treatment) which will contain things such as diagnosis and reports on treatment completion.

9.  If you're looking for images, the index you need is the gstt_clinical_epr_results. The accession numbers for the images are stored under the keyword 'document_AncillaryReferenceID'. The accession numbers in this field may sometimes miss some letters, may be amended to include a hyphen, may be missing a number or have a 1 after 'RJ'. This is an indexing issue. If you find error, you can use the scan date and patient MRN to find the relevant imaging. Both will be exported along with the accession number in your CSV file.

10. To save the results of your query and export them for further processing, first save your query by clicking on the saving menu on the left-hand side of the search bar and click on 'Save current query'. Name your query something sensible that will be easy to recognise. Once your query is saved, click on 'Share' on the top right corner, then select 'CSV Report'. You will then be able to export your results in a CSV file.