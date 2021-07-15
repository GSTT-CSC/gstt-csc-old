---
layout: project_description
title: Work
description: What we'll do, are doing, have done
---

# **Early detection of rectal cancer**

| <b>Project Title</b> | A machine learning algorithm to aid in the detection of early rectal cancers/polyps.  |
| <b>Clinical lead(s)</b> | Tina Mistry |
| <b>CSC lead</b> | [Laurence](/team/laurence.html) |
| <b>Rationale</b> | Development of an AI tool to identify areas of concern that may indicate early development of cancer and polyps in rectal MRI images |
| <b>Modality</b> | MRI |
| <b>Pathology</b> | Rectal cancer/polyps |
| <b>Description</b> | MRI pelvis studies are reported by a variety of subspecialty radiologists leading to missed pathology in the rectum outside of the reporter’s immediate comfort zone. The consequence of a missed polyp is the development of later stage cancerous lesions which are more symptomatic and potentially incurable or require extensive surgery/treatment as oppose to minimally invasive endoluminal procedures. An artificial intelligent algorithm has the potential to reduce these errors by highlighting areas of concern particularly within the rectum which can be a challenging area to assess. |
| <b>Patient pathway</b> | Once a lesion is identified whether these abnormalities are cancerous or polyps the ultimate treatment for this is removal which is curable if performed early. |
| <b>Training datasets</b> | Large MRI pelvis dataset within the trust with the T2 weighted axial and diffusion performed in most cases. This will give a high yield of normal. Rectal cancer datasets also collected via a recent audit. |
| <b>Consequences of errors | False positives will either result in early interval repeat imaging or proctoscopy performed by surgeons in clinic/endoscopy. False negative may result in cancers being detected at a later stage. |
| <b>Goals</b> | An application that is able to identify areas of concern for further analysis by radiologists |
| <b>Criteria for success</b> | Ability to identify lesions incidentally/early leading to improved outcomes for patients, early detection leads to stopping/reducing the development of malignancy which can be fatal when diagnosed at a late stage. |
| <b>Commercial products available</b> | None identified |
| <b>References</b> | [1] Lee, Joohyung, et al. "Reducing the model variance of a rectal cancer segmentation network." IEEE Access 7 (2019): 182725-182733. [online](https://arxiv.org/pdf/1901.07213.pdf) |

___

*The plan below aims to outline the expected outcomes for each stage of the project development cycle.*
### Project Plan
**Planning phase**
1. Meeting of all persons involved to determine AI specifications
    1. Agree project plan
    2. Setting technical and system requirements for AI model
    3. Agree on most useful metrics for success – e.g. percentage reduction in missed polyps
        * step change in number of reported polyps
        * This will require designing a fixed methodology for measuring currently missed polyps which can be performed before and after model deployment.
    4. Agree on minimum valuable requirements for success e.g. 25% reduction in missed polyps
        * We are aiming for a 10% reduction in missed polyps using the methodology above.
    5. Agree on size of POC and production datasets and who is responsible for compiling them
        * We will use existing database of 5 year audit to generate proof-of-concept dataset
    6. Agree on how model will be deployed
        * The application will push information back to radiologist workstation to indicate suspect dicom series as well as slice number and region

**Development phase (proof of concept (POC))**
2. Dataset curation (retrospective)
    1. Compile POC dataset
3. Model training
    1. Produce effective POC model
4. Model testing
    1. Test model against agreed criteria for success (where applicable)
    2. Agreement to continue to production phase OR iterative/improve model OR discontinue

**Development phase (production)**
5. Dataset curation (retrospective)
    1. Compile larger production dataset with all appropriate data properties (e.g. ethnicity, weight etc)
6. Model training
    1. Produce effective deployment model
7. Model testing
    1. Test model against agreed criteria for success (where applicable)
    2. Clinical approval for model to be deployed

**Deployment phase**
8. Deployment to test environment (if applicable)
    1. Testing successful
9. Deployment to hospital systems
    1. Training for users
    2. Continuous monitoring of model performance
