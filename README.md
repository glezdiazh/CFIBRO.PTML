# CFIBRO.PTML
Advancing Cystic Fibrosis Care with Artificial Intelligence


# Authors
Carmen Velázquez1,#, María D. Pastor-Vivero2,#,*, Estefanía Ascencio-Medina3,4,#, 
José Ángel Fernández-Higuero5, Maialen Zabala1, Aliuska Duardo-Sánchez6, Ane Ibañez-Antolín7, Jon Altuna-Álvarez1,, Amaia González-Magaña1,8, Itxaso Montánchez9, Patricia Iraurgui-Arcarazo2, Ainhoa Gómez-Bonilla2, Félix Baranda García2, Sonia Arrasate7, David Albesa-Jové,1,8,10,* Humberto González-Díaz1,7,10*



# Affiliations
1 Instituto Biofisika (CSIC, UPV/EHU), Fundación Biofísica Bizkaia/Biofisika Bizkaia Fundazioa, 48940 Leioa, Spain.
2 Cruces University Hospital, Biobizkaia Health Research Institute, 48903 Barakaldo, Spain.
3 Department of Computer Science and Information Technologies, Faculty of Computer Science, CITIC-Research Center of Information and Communication Technologies, University of A Coruña, 15071 A Coruña, Spain.
4 IKERDATA S.L., ZITEK, University of Basque Country UPVEHU, Rectorate Building, 48940 Leioa, Spain.
5 Jesuitak Politeknikoa, 48010 Bilbao, Spain.
6 Department of Public Law, University of the Basque Country (UPV/EHU), 48940 Leioa, Spain.
7 Department of Organic and Inorganic Chemistry, University of the Basque Country (UPV/EHU), 48940 Leioa, Spain.
8 Department of Biochemistry and Molecular Biology, University of the Basque Country (UPV/EHU), 48080 Bilbao, España.
9 Department of Immunology, Microbiology, and Parasitology, University of the Basque Country (UPV/EHU), 48940 Leioa, Spain. 
10 Ikerbasque, Basque Foundation for Science, 48013 Bilbao, Spain

(#) These authors contributed equally to this work
* To whom correspondence should be addressed: David Albesa-Jové, Humberto González-Díaz and María D. Pastor-Vivero
E-mails: 
david.albesa@ehu.eus, 
humberto.gonzalezdiaz@ehu.es, 
mariadolores.pastorvivero@osakidetza.eus 

# Abstract
Cystic Fibrosis (CF) is a genetic disorder characterized by dysfunctional ion transport leading to thick mucus secretion and chronic pulmonary infections. Current treatment relies heavily on antibiotics, guided by antibiotic susceptibility testing, which often lacks correlation with clinical outcomes due to the complex multifactorial nature of CF pulmonary disease. In this longitudinal study, we analyse the sputum samples from 48 CF patients using Next Generation Sequencing to track microbial changes alongside clinical outcomes over a period of six months. Additionally, we develop an Artificial Intelligence algorithm that integrates multiple clinical variables including bacteriome composition to predict clinical outcomes. Our findings underscore the potential of AI-driven approaches in CF clinical practice, offering insights into disease dynamics, treatment optimisation, and personalised medicine. Furthermore, we address data privacy concerns by introducing a Monte Carlo Synthetic Data methodology, ensuring General Data Protection Regulation compliance while preserving data robustness. Overall, our study enhances understanding of CF pathophysiology and highlights the potential of AI in improving patient outcomes.



# Personal Data Protection

All data management and analysis were in compliance with the General Data Protection Regulation (GDPR). GDPR defines pseudonymization in Article 4 (5) as: 'the processing of personal data in such a way that they can no longer be attributed to a data subject without the use of additional information, provided that such additional information is kept separately and is subject to technical and organizational measures intended to ensure that the personal data are not attributed to an identified or identifiable natural person'. In general terms, pseudonymization aims at protecting personal data by hiding the identity of individuals (data subjects) in a data set, for example by replacing one or more personal data identifiers with so-called pseudonyms and by adequately protecting the link between the pseudonyms and the initial identifiers. Consequently, all patient data was pseudonymized by the team of the Biocruces Foundation by using an internal code to identify the patients. These codes and the identities of patients were never shared with the other researchers in this paper or the public in general. 

# Supporting Information
Supporting information files contain the following information:

Supporting Information file SI00.doc
Under construction

Supporting Data SI01_PCRIFPTML-LDA Results, last 2024_jan_24
Supporting Data SI02_PCRIFPTML-MCSD model, last 2024_jan_24
Supporting Data SI03 PCRIFPTML MC Synthetic Data, last 2024_jan_24
Supporting Data SI04_ PCRIFPTML-LDA heatmap, last 2024_feb_21
Under construction

# ANN code
Supporting information file IFPTML-ANN-CFIBRO.c contain the code in c language of the ANN models trained and validated in this paper. The code of the software used to generate the models is part of the STATISTICA package an is not propietary of the authors for release. The code may be used to implement the model in other software ever following the licence specifications by Statsoft inc. specified inside these files. Please in case you want to obtain similar ANN models use this package or other ANN algorithms package implemented in Phyton, WEKA, or other algorithms. In any case, we would like to point out that the linear models presented in the paper are simpler and have similar to better statistical performance than the ANN models released here. If your objective is using our models to predict new fuel blends we recommend the linear models instead of the ANN models released here. This linear models can be run in Excel or in any other script using the linear equations presented in the paper. You can reproduce the models using the data released at follows in the Supporting information files.

# Funding
The authors acknowledge financial support from the Basque Government's Department of Health (Research Projects 2022333042, 2020333031, and 2021333049). H.G.-D. thank the financial support of the Research Project AIMOFGIFT -KK-2022/00032- funded by the Basque Government, Department of Economic Development, Sustainability and Environment, through the program of aid for Collaborative Research in strategic areas. D.A.-J. acknowledges support by the MICINN Contract PID2021-127816NB-I00, Fundación Biofísica Bizkaia, the Basque Excellence Research Centre (BERC) program, and IT1745-22 of the Basque Government. M.Z. and J.A. acknowledges support from the Basque Government predoctoral program. We thank Dr. Adrián Odriozola and Nerea Vallejo (University of the Basque Country) for their support in NGS and critical reading of the manuscript.

# References
Under construction


