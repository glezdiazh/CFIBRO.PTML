# CFIBRO.PTML
Towards Advancing Cystic Fibrosis Care with Artificial Intelligence


# Authors
Estefanía Ascencio-Medina1,2,#, María D. Pastor-Vivero3,#,*, Carmen Velázquez4,#, José Ángel Fernández-Higuero5, Maialen Zabala-Zearreta4, Aliuska Duardo-Sánchez6, Ane Ibañez-Antolín7, Patricia Iraurgui-Arcarazo3, Shan He7, Sonia Arrasate7, David Albesa-Jové,4,8,10,*, Humberto González-Díaz1,7,9*, and the CF-Study Working Group

The CF-Study Working Group consists of the authors and Ainhoa Gómez-Bonilla, Félix Baranda-García, Jon Altuna-Alvarez, Amaia González-Magaña, and Itxaso Montánchez.


# Affiliations
1 Department of Computer Science and Information Technologies, Faculty of Computer Science, CITIC-Research Center of Information and Communication Technologies, University of A Coruña, 15071 A Coruña, Spain.
2 IKERDATA S.L., ZITEK, University of Basque Country UPVEHU, Rectorate Building, 48940 Leioa, Spain.
3 Cruces University Hospital, Biobizkaia Health Research Institute, 48903 Barakaldo, Spain.
4 Instituto Biofisika (CSIC, UPV/EHU), Fundación Biofísica Bizkaia/Biofisika Bizkaia Fundazioa, 48940 Leioa, Spain.
5 Jesuitak Politeknikoa, 48010 Bilbao, Spain.
6 Department of Public Law, University of the Basque Country (UPV/EHU), 48940 Leioa, Spain.
7 Department of Organic and Inorganic Chemistry, University of the Basque Country (UPV/EHU), 48940 Leioa, Spain.
8 Department of Biochemistry and Molecular Biology, University of the Basque Country (UPV/EHU), 48080 Bilbao, España.
9 Ikerbasque, Basque Foundation for Science, 48013 Bilbao, Spain


(#) These authors contributed equally to this work
(*) To whom correspondence should be addressed: David Albesa-Jové, Humberto González-Díaz and María D. Pastor-Vivero
E-mails: 
david.albesa@ehu.eus, 
humberto.gonzalezdiaz@ehu.es, 
mariadolores.pastorvivero@osakidetza.eus 

# Abstract
Cystic Fibrosis (CF) is an autosomal recessive genetic disorder caused by mutations in the CFTR gene, leading to dysfunctional chloride and other ion transport [1, 2]. This results in thick mucus secretions and chronic pulmonary infections [3]. Traditional treatment approaches rely on antibiotic susceptibility testing (AST), which often fails to correlate with clinical outcomes due to the complex and multifactorial nature of CF infections.

During childhood infections are commonly produced by Staphylococcus aureus and Haemophilus influenzae, while in adults, Pseudomonas aeruginosa, Stenotrophomonas maltophilia or Burkholderia spp predominate [4]. However, up to 80% of patients suffer from chronic infection of P. aeruginosa [5], and the acquisition of the organism coincides with a decline in clinical condition [6–9].  Current treatment guidelines for CF recommend antibiotics for a variety of clinical scenarios, including eradication of early infection with P. aeruginosa, suppressive therapy of chronic airway infection due to P. aeruginosa, chronic macrolide therapy to reduce exacerbations, and intermittent use of antibiotics to treat pulmonary exacerbations (PEx) [10]. The choice of antibiotic therapy administered to each patient depends on the antibiotic resistance profile obtained from a routine practice where sputum is analysed during an exacerbation [11]. Nonetheless, the usefulness of antibiotic susceptibility testing (AST) is unclear to date as there is a poor correlation between in vitro results and clinical outcomes. This is most likely related to the fact that the standard AST is designed to be applied to a single bacterial species cultured in the context of an acute infection, not to a community of microorganisms causing a chronic polymicrobial infection [10, 12].

Furthermore, lung activity in CF patients is shaped by various factors, including host immune responses, pathogen colonization, inflammation, treatments, genetics, and environmental influences, all contributing to the complexity of the disease [13, 14]. However, the analysis and interpretation of large datasets present new challenges that could be addressed using Artificial Intelligence/Machine Learning (AI/ML) models. 


# Patient enrolment and sample/data collection

Entrants into this study were restricted to CF patients who possessed verifiable records confirming their CF diagnosis and who bore no history of undergoing lung transplantation. Ethical endorsement for this study was procured from the ethics committee of University Hospital of Cruces (Barakaldo, Spain) and the University of the Basque Country’s ethics committee (Leioa, Spain). Preceding the incorporation into the study, patients and, if pertinent, their parents or guardians were comprehensively apprised of the study's nature, and their informed consent or assent, contingent on age, was duly procured. 

Collection of pharyngeal swab and sputum specimens was undertaken, giving precedence to the latter where patient expectoration capacity allowed. The entire process of specimen procurement was entirely voluntary, with meticulous attention to the safeguarding of personal data and the utmost confidentiality of patient information. The initiative of sample procurement transpired over a duration of six months, characterised by a recurring temporal frequency of a singular sample per patient, with intervals of three months demarcating each collection episode.

Integral data encompassing variables such as age, gender, stature, CFTR mutation, antecedent pathologies including but not limited to pancreatitis, diabetes, and liver disease, the occurrence or non-occurrence of exacerbations, nutritional status, lung function indices (FEV1 and FVC or Forced Vital Capacity), as well as prior incidents of infections and antibiotic treatments have all contributed substantively to the scope of data acquisition.

# Computational Methods 

# Personal Data Protection

All data management and analysis were in compliance with the General Data Protection Regulation (GDPR). GDPR defines pseudonymization in Article 4 (5) as: 'the processing of personal data in such a way that they can no longer be attributed to a data subject without the use of additional information, provided that such additional information is kept separately and is subject to technical and organizational measures intended to ensure that the personal data are not attributed to an identified or identifiable natural person'. In general terms, pseudonymization aims at protecting personal data by hiding the identity of individuals (data subjects) in a data set, for example by replacing one or more personal data identifiers with so-called pseudonyms and by adequately protecting the link between the pseudonyms and the initial identifiers. Consequently, all patient data was pseudonymized by the team of the Biocruces Foundation by using an internal code to identify the patients. These codes and the identities of patients were never shared with the other researchers in this paper or the public in general. 

![image](https://github.com/user-attachments/assets/ee51d9ed-ec8e-4123-87ce-a7e6d82e5c1c)


# Supporting Information
Supporting information files contain the following information:

Under construction

# Funding
The authors acknowledge financial support from the Basque Government's Department of Health (Research Projects 2022333042, 2020333031, and 2021333049). H.G.-D. thank the financial support of the Research Project AIMOFGIFT -KK-2022/00032- funded by the Basque Government, Department of Economic Development, Sustainability and Environment, through the program of aid for Collaborative Research in strategic areas. D.A.-J. acknowledges support by the MICINN Contract PID2021-127816NB-I00, Fundación Biofísica Bizkaia, the Basque Excellence Research Centre (BERC) program, and IT1745-22 of the Basque Government. M.Z. and J.A. acknowledges support from the Basque Government predoctoral program. We thank Dr. Adrián Odriozola and Nerea Vallejo (University of the Basque Country) for their support in NGS and critical reading of the manuscript.

# References
Under construction


