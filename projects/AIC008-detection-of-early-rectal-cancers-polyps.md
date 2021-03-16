# Early detection of rectal cancer

| Project Title | A machine learning algorithm to aid in the detection of early rectal cancers/polyps.  |
| --- | --- |
| Clinical lead(s) | - |
| --- | --- |
| CSC lead | Laurence Jackson |
| --- | --- |
| Rationale | Development of an AI tool to identify areas of concern that may indicate early development of cancer and polyps in rectal MRI images |
| --- | --- |
| Modality | MRI |
| --- | --- |
| Pathology | Rectal cancer/polyps |
| --- | --- |
| Description | MRI pelvis studies are reported by a variety of subspecialty radiologists leading to missed pathology in the rectum outside of the reporter’s immediate comfort zone. The consequence of a missed polyp is the development of later stage cancerous lesions which are more symptomatic and potentially incurable or require extensive surgery/treatment as oppose to minimally invasive endoluminal procedures. An artificial intelligent algorithm has the potential to reduce these errors by highlighting areas of concern particularly within the rectum which can be a challenging area to assess. |
| --- | --- |
| Patient pathway | Once a lesion is identified whether these abnormalities are cancerous or polyps the ultimate treatment for this is removal which is curable if performed early. |
| --- | --- |
| Training datasets | Large MRI pelvis dataset within the trust with the T2 weighted axial and diffusion performed in most cases. This will give a high yield of normal. Rectal cancer datasets also collected via a recent audit. |
| --- | --- |
| Consequences of errors | False positives will either result in early interval repeat imaging or proctoscopy performed by surgeons in clinic/endoscopy. False negative may result in cancers being detected at a later stage. |
| --- | --- |
| Goals | An application that is able to identify areas of concern for further analysis by radiologists |
| --- | --- |
| Criteria for success | Ability to identify lesions incidentally/early leading to improved outcomes for patients, early detection leads to stopping/reducing the development of malignancy which can be fatal when diagnosed at a late stage. |
| --- | --- |
| Commercial products available | None identified |
| --- | --- |
| Project Plan | 1.	Meeting of all persons involved to determine AI specifications <br><br> 2.Setting technical and system requirements for AI model <br><br> 3.Dataset curation (retrospective) <br><br> 4.Model training <br><br> 5.Model testing <br><br> 6.Implementation |
| --- | --- |
| References | [1] Lee, Joohyung, et al. "Reducing the model variance of a rectal cancer segmentation network." IEEE Access 7 (2019): 182725-182733. [online](https://arxiv.org/pdf/1901.07213.pdf) |