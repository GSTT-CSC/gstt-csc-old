---
layout: project_description
title: Work
description: What we'll do, are doing, have done
---

# **Rotational profiles**

| <b>Project Title</b> | Assessment of rotational profiles in lower limb CT for pre surgical assessment |
| <b>Clinical lead(s)</b> | Dr. Christopher Tang  |
| <b>CSC lead</b> | [Anil](/team/Anil.html) |
| <b>Rationale</b> | Assessment of rotational profiles is time consuming and complex. An AI algorithm would significantly decrease the amount of time needed to measure the angles of rotation. |
| <b>Modality</b> | CT |
| <b>Pathology</b> | Lower limb rotation |
| <b>Description</b> | Current practice of manually drawing lines over the long bones and the joints on CT images in PACS to figure the degree of misalignment is time-consuming (15-20 minutes per case). An AI tool would automatically create these lines and angles, saving time and reducing variability. |
| <b>Patient pathway</b> | Patients are referred by the orthopaedic team. CT imaging is part of the pre-surgical work up. The report is used to plan the surgical intervention. |
| <b>Training datasets</b> | Over 100 patients are referred annually. The data will be retrospective, acquiring a large cohort of patients and segmentation and profile results as annotated on PACS. It is possible annotations will need to be re-done if they cannot be exported from PACS. |
| <b>Consequences of errors</b> | The tool is to help find the accurate rotational profile and will be supervised and signed off by the radiologist, so an error is unlikely to persist far enough to affect a patient. |
| <b>Goals</b> | Reduction of radiologist time in reporting these scans as well as increase consistency in calculation. |
| <b>Criteria for success</b> | Accurate, automated rotational profiles. |
| <b>Commercial products available</b> | N/A |
| <b>Project Plan</b> | <b> 1.	Meeting of all persons involved to determine AI specifications.</b> <br><br> For radiologist (Chris) :<br> - [ ] Confirm +/3 to 5 degree precision with peers<br> - [ ] Confirm with surgeons how angles are used to guide knee surgery <br> - [ ] Confirm 3 bone ankle slice is the correct slice to analyse.<br>- [ ]   Review software requirements spec <br> <br><b>2.	Setting technical and system requirements for AI model.</b><br><br> For CSC (Anil) <br>  - [ ]  Perform the risk assessment<br> - [ ] Create software design spec from software requirements spec <br> - [ ] Attempt to build non-A.I software with “dicom_server” and eventually “AI Deployment Engine” <br> - [ ] Investigate the AI route<br><br><b> 3. Dataset curation (retrospective). </b><br><br> - [ ] Collect Patient ID’s for 100-200 patients, analysed by different radiologists<br><br> <b>4.	Model training</b><br><br> <b>5.	Model testing</b> <br><br><b>6.	Implementation</b> <br><br><b>7. Audit </b> |
| <b>References</b> | Website used to help calculate rotational angles is <a href="http://uwmsk.org/legrotation.html"> here</a>. |