# **Synthetic CT for MR-Only Prostate Radiotherapy Planning**

| Project Title | AI to create a Synthetic CT for MR-Only Prostate Radiotherapy Planning|
| --- | --- |
| <b>Clinical lead(s)</b> |  Christopher Thomas|
| --- | --- |
| <b>CSC lead</b> | [Anil](/team/anil.html) |
| --- | --- |
| <b>Rationale</b> | MRI gives superior soft tissue contrast compared to CT images which allows more accurate contouring of internal organs and tumours for radiotherapy (RT). Only CT images, however, provide the voxel electron density data needed to calculate the dose distribution from radiation beams. Having an MRI with electron density information in the form of a “synthetic CT” (SynCT) would streamline imaging, reduced concomitant imaging dose, and improve contouring tumours and organs, thus reducing unnecessary dose to healthy tissues which is linked to reduced toxicity and complications post-treatment.    |
| --- | --- |
| <b>Modality</b> | Radiotherapy CT, MRI|
| --- | --- |
| <b>Pathology</b> | T3N0 Prostate Cancer |
| --- | --- |
| <b>Description</b> |Patients prescribed radiotherapy to the prostate have a CT scan which provides anatomical information used to target the RT, and electron density info required for dose calculation in the treatment planning system (TPS). The patient’s RT plan is generated using the CT scan and the plan is sent to the treatment machine. Prostate RT patients experience toxicity side-effects due to irradiation of healthy tissues including rectum rectum, bladder, urethra and penile bulb. Doses to these tissues are higher than they could be due to uncertainties in defining the prostate treatment volume on CT, where studies show that delineation of the prostate on MR results in 25-40% reduction in prostate volume [2-5] with more consistency between operators [6-9]. <br><br> An in-house study at GSTT has shown that rectal and bladder dose can be reduced, and this should relate to a reduction in toxicity risk. The improved soft-tissue contrast of MRI can be used to better define targets and additional healthy tissue [10]. Ideally an MR-only pathway is used, where the MRI is used for anatomical delineation and for dose calculation. A benefit of MR-only RT is the removal of registration uncertainties [12] present in a combined CT + MRI pathway. MRI data has no inherent electron density information so for an MR-only pathway to be feasible a SynCT must be made for the TPS dose calculation.|
| --- | --- |
| <b>Patient pathway</b> | Currently, patients receiving radiotherapy for prostate cancer T3N0 undergo CT imaging, where the patient is in the RT treatment position on an identical treatment couch. If MRI is also required for improved soft tissue delineation, then a RT MRI is acquired at Guys Cancer Centre, with an identical treatment couch. The CT and MRI are both imported into the TPS, registered into the same reference frame, then contoured by the clinician.<br>The proposed project would allow the RT MRIs, generated from a set protocol, to be automatically sent to a ML model (in “dicomserver” or “AI Deployment Engine”) that would generate a SynCT which automatically transfers to a input folder for the treatment planning software. ||
| --- | --- |
| <b>Training datasets</b> | 35 patients with MR and CT images, pseudonymised, as part of <a href= "https://clinicaltrials.gov/ct2/show/NCT03238170"> clinical trial (NCT03238170)</a>  |
| --- | --- |
| <b>Consequences of errors</b> | Dose distributions from the RT treatment plans would be incorrectly calculated which could result in poor treatment efficacy and increase toxicity to healthy tissues.  |
| --- | --- |
| <b>Goals</b> | To implement a model that can assign Hounsfield units (related to electron density) to voxels in MR image sets for prostate RT planning, in a way that provide little to no interaction from radiotherapy staff & clinicians.  |
| --- | --- |
| <b>Criteria for success</b> | Reduction of healthy tissue dose and toxicity risk in patients receiving RT to the prostate. |
| --- | --- |
| <b>Commercial products available</b> | Philips MRCAT (MR for Calculating ATtenuation) <br><br>Siemens syngo.via RT Image Suite|
| --- | --- |
| <b>Project Plan</b> | 1.	Meeting of all persons involved to determine AI specifications. <br><br> 2.	Setting technical and system requirements for AI model. <br> <br> 3. Dataset curation (retrospective). <br><br> 4.	Model training<br><br>5.	Model testing <br><br>6.	Implementation <br><br>7. Audit|
| --- | --- |
| <b>References</b> | [1] <a href=" https://www.cancerresearchuk.org/health-professional/cancer-statistics/statistics-by-cancer-type/prostate-cancer" > CRUK prostate Cancer Statistics</a><br>[2] <a href = "https://doi.org/10.1016/s0360-3016(98)00351-4"> Rasch et al. 1997</a><br>[3] <a href = "https://doi.org/10.1259/bjr.75.895.750603"> Sannazzari et al. 2014</a><br>[4] <a href = "https://doi.org/10.1016/0360-3016(96)00232-5"> Roach et al. 1996</a><br>[5] <a href = "https://doi.org/10.1016/s0360-3016(96)00620-7"> Kagawa et al. 1997</a><br>[6] <a href = "https://doi.org/10.1016/s0360-3016(99)00288-6" > Debois et al. 1999 </a><br>[7]<a href = "https://doi.org/10.1016/s0167-8140(02)00407-3"> Parker et al. 2003 </a><br>[8]<a href = "https://doi.org/10.1259/bjr.20180948"> Pathmanathan et al. 2019</a><br>[9]<a href = "https://doi.org/10.1016/j.ijrobp.2010.03.019"> Usmani et al. 2011</a><br>[10]<a href = "https://doi.org/10.1186/1748-717x-7-82"> Vainshtein et al. 2021</a><br>[11]<a href = "https://doi.org/10.1016/j.rcl.2017.10.012"> Menard et al. 2018</a><br>[12]<a href = "https://doi.org/10.1186/1748-717x-4-54"> Nyholm et al. 2009</a><br>[13]<a href = "https://doi.org/10.1016/j.ijrobp.2017.08.043"> Johnstone et al. 2018</a><br>[14]<a href = "https://doi.org/10.1016/S0167-8140(21)01769-2"> Thomas et al. 2020</a><br>[15]<a href = "https://doi.org/10.1016/j.ijrobp.2019.06.2530"> Bird et al. 2019</a><br>[16]<a href = "https://doi.org/10.1016/j.phro.2019.11.005"> Wyatt et al. 2019</a><br>|
 |