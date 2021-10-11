# **Workshop: The Problem of Bias in AI**
<br>
The CSC team held a workshop on racial bias in AI and strategies to combat it on 2nd June 2021. As part of the preparation the team watched the Netflix documentary Coded Bias which discusses facial recognition bias in AI technology as experienced and published by Joy Buolamwini. More on her and her team’s work can be found <a href="https://www.ajl.org">here</a>. 
<h2>The Case Studies</h2> 
<br>
The session started with a broad overview of the problem of bias in AI, focussing on the following four case studies:
<br>
<ol>
<li>Facial Recognition
<ul>AI algorithms have been preferentially trained on examples of faces of lighter-skinned individuals leading to algorithm’s inability to accurately ‘recognise’ a darker-skinned individual. The example of this used in the documentary is Amazon’s facial recognition software that Joy tried to use for her thesis which could not recognise her face as a face until she put on a white mask. Without trivialising the obvious dehumanising effects this has on the individuals not recognised as humans and the urgency in algorithm re-training, we focussed on the practical applications of this and similar software in the real world now, primarily in facial recognition AI software used in policing. An AI algorithm less accurate in recognition of darker-skinned individuals is more likely to lead to innocent people of colour being identified by the software and subsequently persecuted and traumatised by the police forces – this is of particular concern in groups which have already been historically subjected to <a href="https://www.statewatch.org/news/2020/september/uk-unmasking-facial-recognition-an-exploration-of-the-racial-bias-implications-of-facial-recognition-surveillance-in-the-united-kingdom/">over-policing</a>. With the above in mind, facial recognition software for police usage is likely to be banned in the EU after <a href="https://edpb.europa.eu/news/news/2021/edpb-edps-call-ban-use-ai-automated-recognition-human-features-publicly-accessible_en">some proposals</a> to that effect have been made. In the USA, where this problem is particularly well documented, Amnesty International has launched a ‘<a href="https://www.amnesty.org/en/latest/press-release/2021/01/ban-dangerous-facial-recognition-technology-that-amplifies-racist-policing/">Ban the Scan</a>’ initiative in January 2021 but no laws currently exist to ban such software. Some calls for ban of such technologies has also been recorded in the UK but has met with more <a href="https://www.ft.com/content/79223f6e-a772-4e74-b256-88641a416f92">hesitancy from government</a> officials.</ul>
</li>
<li>Health Insurance AI (USA)
<ul>We discussed the paper by <a href="https://www.science.org/doi/abs/10.1126/science.aax2342">Obermayer et al (2019)</a> which detailed an analysis of an AI algorithm used for prediction of patients at risk of potential complications and need for intervention. The algorithm highlighted Black patients as in need for intervention when they were much more ill than White patients, systematically discriminating based on race. This AI algorithm is in use in USA and has affected millions of patients already. The system was not coded to distinguish between patients by race – in fact, the information on race was deliberately excluded, but the total healthcare cost incurred in a year was used as a surrogate measure for healthcare needs and number of chronic conditions. The algorithm designers and developers failed to account for differences in the way healthcare systems are accessed in USA and how that ties in with race, socioeconomic background and location. The system therefore failed to account for systemic discrimination embedded in society and produced an algorithm that furthered it.</ul>
</li>
<li>Chest X-Ray
<ul>We discussed a case of a chest x-ray algorithm which was trained on publicly available datasets which contained significantly more male patients than female patients which resulted in an algorithm less accurate for <a href="https://www.pnas.org/content/117/23/12592">female patients than male patients</a>.</ul>
</li>
<li>Dermatology
<ul>We discussed the ongoing issue in dermatology of under-representation of darker-skinned individuals in training, testing and treatment. This problem is well documented: there is a critical lack of representative imagery in training dermatologists to recognise rashes, skin conditions and melanoma, which leads to under-diagnosis and under-treatment of darker-skinned individuals (<a href="https://jamanetwork.com/journals/jamadermatology/article-abstract/2782060">for example</a>, invasive melanoma is much rarer in Black patients but it is far more likely to be fatal due to diagnostic delays). There is substantial warning, discussion and debate on this topic in medical AI circles and the <a href="https://www.theatlantic.com/health/archive/2018/08/machine-learning-dermatology-skin-color/567619/">steps needed to prevent this practice</a> from being translated into AI. Further, AI is a great opportunity to counteract the bias by ensuring sufficient data on darker-skinned individuals is included in the training and testing datasets.</ul>
</li>
</ol>
<br>
<h2>Root Causes of Health Injustice</h2>
<br>
Then we discussed the origins of health injustice across the globe by focussing on the following four points:
<br>
<ol>
<li>Global health injustice
<ul>The 10/90 gap is a term commonly used in global discussions on health research to highlight that less than 10% of total worldwide health research funding is devoted to illnesses that affect 90% of the global population, particularly as the majority of those illnesses disproportionately affect poorer populations or populations in poorer countries. The amount of focus, funding and data is therefore likely to serve populations already well served – this should be kept in mind when choosing which problems should be solved first.</ul>
</li>
<li>Racial Injustice
<ul>The 10/90 gap can be found in research which focuses on genetic disorders which are related to race. The example we discussed is sickle cell anaemia, a genetic disorder that affects predominantly Black patients, and cystic fibrosis, a genetic disorder that affect predominantly White patients. Cystic fibrosis research is <a href="https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2763606">substantially better funded that sickle cell anaemia research</a>, resulting in more research articles published and more treatments approved by the FDA.</ul>
<ul>Maternal death and negative outcomes associated with pregnancy and childbirth are significantly higher in people of colour than in White people. This trend can be observed both in the UK and the USA and has worsened over time. The root cause of this disparity is not clear and so the remedy for this discrepancy is not straightforward. Speculatively and anecdotally, the reason for worse outcomes can be tied to structural racism which affects people of colour in their everyday lives in the way they access healthcare, the way they are treated within healthcare services, the way they interact with community support and so on.</ul>
</li>
<li>Gender Injustice
<ul>Menstrual health affects approximately half of the population for a significant portion of their lifetime but is largely stigmatised as a topic of conversation and underrepresented as a topic for research. A disease-specific example is endometriosis which is a common and painful condition affecting an estimated 10% of menstruating population worldwide but which is chronically under-diagnosed, largely unstudied and for most individuals remains untreated throughout their lives even though the pain associated with the condition can be debilitating.</ul>
<ul>Healthcare of transgender people is still not a focus in global research, despite hormone replacement therapies being associated with higher incidence of some gender-specific cancers (such as breast and prostate cancers) and despite an increase in HIV/AIDS prevalence in transgender sex workers. Transgender people are frequently missed from screening services and face systemic discrimination when seeking healthcare worldwide.</ul>
</li>
<li>Diversity of the scientific workforce
<ul>Scientific workforce worldwide is not diverse and lacks in gender, racial and socioeconomic representation. It is still predominantly white, male and has origins associated with higher socioeconomic status. Non-wealthy and non-white individuals are still very weakly represented in academia as well as boards in tech industry and healthcare boards, including in the NHS. The obvious problem this creates is that many marginalised groups do not have sufficient advocacy at decision-making levels and are thus insufficiently served by the community and sometimes entirely omitted from the conversation, intentionally or unintentionally. </ul>
</li>
</ol>
<br>
<h2>The Solutions</h2>
<br>
The strategies most commonly advised in literature as methods of avoiding bias in data, whether gender, socioeconomic or racial are the following:
<br>
<ol>
<li>
<b>Diversity in data:</b>
<ul>The data collected for algorithm training purposes needs to be representative and include all potential patients, ideally in equal measure (i.e. 'the real world data').
</ul></li>
<li><b>Diversity in validation:</b>
<ul>
The data collected for algorithm testing must include sufficiently representative sample of patient data, including any minority or marginalised group that may be subjected to the algorithm’s decision-making. The algorithm must perform equally well across all relevant patient groups.
</ul>
</li>
<li><b>Diversity in people:</b> 
<ul>
It is crucial that the team designing, training and developing algorithms is diverse in gender, socioeconomic, religious and/or ethnic background to ensure advocacy from design until deployment and beyond for as many patient groups as possible.
</ul>
</li>
</ol>
<br>
<h2>Our Problem</h2>
<br>
<ol>
<li>We use ‘real data’ – using medical data and not publicly available, purchased or volunteered datasets means our data captures all service users. But is this enough to ensure no bias in our algorithms?</li>
<li>We have a diverse patient population – we are part of an NHS institution with long history of healthcare provision across some of the most locally diverse populations in the world. Our data is therefore representative of an incredibly diverse population, acquired as part of standard of care. But is this enough?</li>
<li>We have a diverse team – we are of different genders, socioeconomic background, religious backgrounds, sexuality and of different ethnicities. But is this enough?</li>
<li>How much data is enough data – we are all trained as scientist understanding a ‘representative sample’ is one where the demographic proportions in the sample are matched to the demographic proportions in the population. This approach to data gathering is not appropriate in AI where the aim of the sample is not to represent the population but to sufficiently represent all members of the population. But how do we ensure this?</li>
</ol>
<br>
<h2>The Discussion</h2>
<br>
The above was followed by a two-hour discussion. We discussed examples where similar biases were seen, not only in AI but healthcare in general; we discussed the nature of AI algorithms in medicine; we discussed the way in which AI will change patient-clinician interaction and the impact that automation of services has on quality of service and quality of care.
<br>
<br>
We formed the following salient points and plans:
<ol>
<li>There must be transparency in all our training and testing data – race and gender of the participant data must be documented.
<ol>Further to above point we explored the data which is collected by our EPR system. Historically data on race in hospitals was not recorded for each patient (though it may be recorded by GP services) and it would be an act of injustice to require this information from some patients (e.g. those we wish to ensure are sufficiently represented such as Black or Asian) but not others (e.g. those we are sure will be sufficiently represented such as White), and equally impractical to call patients and ask them about their race or ethnic background. We spoke of the AI which predicts ethnicity from names but agreed it would be much too inaccurate and likely to be itself biased, and that patient names should not be speculated upon. However, much to our very pleasant surprise, a random sample of patients admitted to the hospital that day showed that around 50% of the patients do have these data recorded and that these data can be accessed by us. It is reasonable to assume that if we can accurately characterise 50% of our training and testing datasets, we can make reasonable assumptions about the other 50% of the data in terms of racial background.</ol>
<ol>Sex is routinely recorded for all patients and is characterised as either M, F or O. While this may not accurately transpose the genders in our selected populations, it will allow us to make reasonable and approximate deductions unless the population studied is such that this deduction does not apply.</ol>
</li>
<li>In any patient population groups which cannot be adequately represented due to lack of data, a disclaimer will be documented and effectively communicated to those using the algorithm (e.g. if the algorithm was trained on very few datasets from Black males, then the clinician will be advised to not use the AI algorithm for that patient but perform the standard of care examination as they would without access to the AI).</li>
<li>Our AI algorithms are trained on local data. We do not expect them to perform well in other situations and on other data and cannot guarantee their performance if exported to other hospitals without re-training.</li>
</ol>

