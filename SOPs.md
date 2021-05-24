---
layout: howto
title: How-to
description: Instructions, SOPs and guides
---

<div class="card" style="width: 100%;">
   <div class="card-body">
      <h5 class="card-title">Contents</h5>
      <ol>
      1. <a href="#QIPS">Registering a project on QIPS</a><br>
      2. <a href="#XNATupload">Uploading data to XNAT</a>
      </ol>
   </div>
</div>


<hr>


## <a name=QIPS></a>**Register your project on QIPS**
`First, make sure that your project falls under 'service development' and not 'research by checking <a href="http://www.hra-decisiontools.org.uk/research/">here</a>. Then, make sure the clinical lead is happy to be added as a collaborator on the QIPS system. Once you're sure of both, proceed to step 1.`

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

2.	Go to https://sv-te-xnat01.gstt.local and log in with your username.

3.	If the project doesn’t exist yet, create it:
    1.	New -> Project -> Fill in the boxes (project title, running title and project ID can be the same word). Add the project description and the investigators (name and email are sufficient). Create the project. Copy and paste the anonymisation script for the project, go to Manage -> Anonymisation Script -> tick Enable Script, and paste it in. You can find it in either other projects or on the share drive. 

4.	The project page will open. On the right-hand side, choose ‘Import From PACS’.

5.	This will open the data query-retrieve (DQR) page which allows you to query Sectra PACS for the requested images. 
    1.	You can use the DQR in two ways: by entering the search criteria or by importing a .csv
        1.	Search criteria: you can use accession number, patient name, patient ID and/or data range and you can use * for wildcard. Click on ‘Search PACS’. Wait for the results to show. Once you find the correct scan, tick in on the left-hand side, and give it a name of the SUBJECT and the name of the SESSION. You need to do this else the patient name will reach XNAT and you’ll have to change the name manually in the pre-archive. Then press the ‘Begin Import’ button at the bottom of the screen. A pop-up will appear to select all images which are relevant. Select all. Click ‘Import’. 
        2.	.csv: you can upload a correctly-formatted csv and it will perform the search for you. This is described here: https://wiki.xnat.org/xnat-tools/dicom-query-retrieve-plugin/using-dqr-bulk-querying-and-importing-via-csv-file. Do not forget to include new SUBJECT and SESSION names: You need to do this else the patient name will reach XNAT and you’ll have to change the name manually in the pre-archive. NB: date style must match query style (ie yyyymmdd) else upload won’t work. Save your file as CSV (Comma delimited) type. Return to XNAT and click on ‘import CSV’ at the top of the page. Choose your csv file. Click on ‘upload’. The query will begin – it may take a while. If an error occurs, test your csv file by reducing it to only one query and see if that comes up with what you expect. Once you can query all you want at once without issue, you’ll have to select which scans to import. NB: XNAT can only handle about 20 import queries at once, else nothing will happen when you click ‘begin import’ (I recommend you do 10 at a time). If you’re importing CTs, de-select the Dose Info, Dose Report and the Patient Protocol series, as those contain burnt-in images of dates and names. Click on ‘Import Selected’. Wait until you get a notification that the query had been sent to PACS. Then click on ‘Close’ and select the next 10 and so on and so on.

6.	The imported data will appear in the pre-archive (Upload -> Go to prearchive). Click ‘Refresh’ if your data isn’t there, or check the Import Queue (Upload ->  Import Queue/History) – the data takes a while to transfer.

7.	In the pre-archive, you can review the details of your import, such as files and DICOM tags. Once you’ve confirmed you’re happy with the data, select it in the pre-archive (tick the left-hand side checkbox) and select ‘Change projects’ on the right-hand side. Select your project. This will assign the data to your project. You can then ‘Archive’ it, which will move the data from the pre-archive into your project folder.

8.	You can now view, amend and interact with the data in the project (Browse -> My Projects -> your folder). You can check the dicom tags of each data session (click on the Subject then hover over the scan details until 3 icons appear – the first is View Details, select this to view tags), you can view the session (click on ‘View Session’ on the right-hand side). You can also delete or download the images here or in the project details. 

