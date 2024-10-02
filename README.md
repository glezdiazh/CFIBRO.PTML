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


# Personal Data Protection

Entrants into this study were restricted to CF patients who possessed verifiable records confirming their CF diagnosis and who bore no history of undergoing lung transplantation. Ethical endorsement for this study was procured from the ethics committee of University Hospital of Cruces (Barakaldo, Spain) and the University of the Basque Country’s ethics committee (Leioa, Spain). Preceding the incorporation into the study, patients and, if pertinent, their parents or guardians were comprehensively apprised of the study's nature, and their informed consent or assent, contingent on age, was duly procured. 

Collection of pharyngeal swab and sputum specimens was undertaken, giving precedence to the latter where patient expectoration capacity allowed. The entire process of specimen procurement was entirely voluntary, with meticulous attention to the safeguarding of personal data and the utmost confidentiality of patient information. The initiative of sample procurement transpired over a duration of six months, characterised by a recurring temporal frequency of a singular sample per patient, with intervals of three months demarcating each collection episode. 

Integral data encompassing variables such as age, gender, stature, CFTR mutation, antecedent pathologies including but not limited to pancreatitis, diabetes, and liver disease, the occurrence or non-occurrence of exacerbations, nutritional status, lung function indices (FEV1 and FVC or Forced Vital Capacity), as well as prior incidents of infections and antibiotic treatments have all contributed substantively to the scope of data acquisition.


# Computational Methods 

# IFPTML model development
In this work, we use the IFPTML strategy to train/validate alternative models able to predict the outcome values vij for each ith patient in different interviews (Ij = I0, I1, I2).  The model can classify the patients according to their personal subset of input continuous variables cj. See a detailed list of variables in Table 1. (https://github.com/glezdiazh/CFIBRO.PTML/issues/1#issue-2560503385).The model also considers the sub-set of personal discrete conditions/labels sj of the patient. See Table 2. (https://github.com/glezdiazh/CFIBRO.PTML/issues/1#issue-2560503385).

As follows, we illustrate the linear form of the IFPTML models and their different cases. The strategy includes three different stages IF, PT, and AI/ML. The general linear form of the IFPTML model to be developed is the following:

# Classic ML linear model (model of order zero).
In this case we use as input the original variables without re-grouping them in distances functions (r = 1, q = 1) and without scaling them with a moving average (α = 0). When we apply the previous constrains the equation of the model can be simplified as follow:

Hyper-parameters: α = 0, q = 1, r = 1, Parameters: a_(c,s) = 0, a_(k,s) = a_k ∈ R

f(v_ij)_calc = a_0 + Σ_(k=1)^kmax [a_k · V_k] #(1.1)

# IFPTML model of order 1.
In this case, we use as input the original variables without re-grouping them into distances functions (r = 1, q = 1), but we do scaling (α = 1). In this scaling we transformed the original variables into first-order PTOs with the form of deviations ∆Vk(sj). These deviations ∆Vk(sj) = Vk - <Vk(sj)> are calculated with a multi-conditional moving average <Vk(sj)>. This multi-conditional moving average takes different values for different groups of patients depending on the sub-set selected sj= sI, sII, or sIII, etc. Please, see Table 2. (https://github.com/glezdiazh/CFIBRO.PTML/issues/2#issue-2560514774). The different possible sub-sets of patients used according to (genetics, genre, treatments, etc.) When we apply the previous constraints, the equation of the model can be simplified as follows:

Hyper-parameters: α = 1, q = 1, r = 1 Parameters: a_(c,s) = 1, a_(k,s) ∈ R

f(v_ij)_calc = a_0 + a_1 · f(v_ij)_ref + Σ_(s=1)^smax Σ_(k=1)^kmax [a_(k,s) · (V_k - <V_k(s_j)>)] (1.2.1)

f(v_ij)_calc = a_0 + a_1 · f(v_ij)_ref + Σ_(s=1)^smax Σ_(k=1)^kmax [a_(k,s) · ∆V_k(s_j)] (1.2.2)

# IFPTML model of order 2.

This is an IFPTML model with PTOs of second order. In this case we use as input the original variables but doing firstly scaling (α = 1) with a multi-conditional moving average ∆Vk(sj) and next re-grouping them (r = 1/2, q = 2) into Euclidean Distances functions ǁ∆Vk(sj)ǁ. This distance was calculated as the square root (r = ½) of the sum of the power two (q = 2) of each deviation. When we apply the previous constraints, the equation of the model can be simplified as follows:

Hyper-parameters: α = 1, q = 2, r = ½  Parameters: a_(k,s) = 1

f(v_ij)_calc = a_0 + a_1 · α · f(v_ij)_ref + Σ_(s=1)^smax [a_(c,s) · {Σ_(k=1)^kmax [V_k - α · (<V_k(c_j)>)]^2 }^(1/2)] (1.3.1)

f(v_ij)_calc = a_0 + a_1 · α · f(v_ij)_ref + Σ_(s=1)^smax [a_(c,s) · ‖∆V_k(s_j)‖_(c_j)] (1.3.3)

In order to seek the different cases of the IFPTML models mentioned above we need to carry out the following IFPMTL data pre-processing stages.  In these stages we are going to explain how to reorganize the data (data engineering) and calculate the values for the objective function f(vij)obs, reference function f(vij)ref, the moving averages <Vk(sj)>, deviations ∆Vk(sj) (first order PTOs), and Euclidean distances ǁ∆Vk(sj)ǁcj. In the following sections we explain in more detail the calculation of the objection function and input parameters of the model, see also the general workflow in Figure 1.(https://github.com/glezdiazh/CFIBRO.PTML/issues/3#issue-2560584698).In all the previous cases, Linear Discriminant Analysis (LDA) could be the algorithm of election to seek this kind of IFPTML linear classification (Hill and Lewicki, 2006).

# IF pre-processing and data rearrangement 
Firstly, we carried out an IF process for both patient clinical data and microbiological data. Patient clinical data (from clinical interviews) included personal data, pharmacological data, genetic data, etc. In contrast, microbiological data come from microbial cultures. Each row (case) corresponds to the ith patient in the rth visit/interview. These columns included four types of variables. The first class of variables vij includes the output values for each patient. The second class Vki are input variables of patients (age, weight, drug doses,…,etc.). 

The third class sj are input/output label variables of patients (gender, …,etc.). The discrete labels sj are of two types: the output variable label s0 and input variable labels sj>0. The output variable label get four different values s0 =Forced Expiratory Volume in 1 second FEV1(%), Forced Vital Capacities FVC(%), Hospitalization Days HD(dd), and days of intravenous antibiotics ATBiv days (dd). The different input discrete variables are organized in the form of a vector sj>0 = [s1, s2, ...s64]. Some of these variables and their values are the following. The first input labeling variable is s1 = Mutations 1, and get the values = ([delta]I507, [delta]F508, Y1092X, etc.) The second labeling variable is s2 = Mutation 2, and get the values = (R334W, [delta]I507, R1066C, G85E, etc.)In total, we have Npatients = 48, Ninterviews = 3, Noutputs = 4 output continuous variables (vij), Nvars = 60 input continuous variables (Vki), and Nlabels = 65 output/input labeling variables (sj). After the initial IF process, we carried out two additional IF and data rearrangement processes. The first was an IF horizontal process and the second and IF vertical process. The IF horizontal process applies to both input labels sj>0 and continuous input variables Vki

# IF horizontal process for input labels
Firstly, we carried an IF process of both patient clinical data and microbiological data. Patient clinical data (from clinical interviews) included personal data, pharmacological data, genetic data, etc. In contrast, microbiological data come from microbial cultures. See the general workflow Figure 1. (https://github.com/glezdiazh/CFIBRO.PTML/issues/3#issue-2560584698).

Each row (case) corresponds to the ith patient in the rth visit/interview. These columns included four types of variables. The first class of variables vij includes the output values for each patient. The second class Vki are input variables of patients (age, weight, drug doses,…,etc.). The third class sj are input/output label variables of patients (gender, …,etc.). The discrete labels sj are of two types: the output variable label s0 and input variable labels sj>0. The output variable label get four different values s0 =Forced Expiratory Volume in 1 second FEV1(%), Forced Vital Capacities FVC(%), Hospitalization Days HD(dd), and days of intravenous antibiotics ATBiv days (dd). The different input discrete variables are organized in the form of a vector sj>0 = [s1, s2, ...s39]. Some of these variables and their values are the following. The first input labeling variable is s1 = Mutations 1, and get the values = ([delta]I507, [delta]F508, Y1092X, etc.) The second labeling variable is s2 = Mutation 2, and get the values = (R334W, [delta]I507, R1066C, G85E, etc.) In total, we have Npatients = 48, Ninterviews = 3, Noutputs = 4 output continuous variables (vij), Nvars = 36 input continuous variables (Vki), and Nlabels = 39 output/input labeling variables (sj). After the initial IF process, we carried out two additional IF and data rearrangement processes. The first was an IF horizontal process and the second and IF vertical process. The IF horizontal process applies to both input labels sj>0 and continuous input variables Vki.

# IF horizontal process for input labels
During the IF horizontal process for input labels, we carried out the following steps. Firstly, we carried out an IF and reorganization/regrouping of the 39 input labels sj>0 = [s1, s2, ...s39] into 7 different subsets or partitions sj>0 = sI&sII&sIII … &sVII. Each one of these partitions is constructed as an IF or regrouping of different input labels, i.e., sI = [s1, s2, s3, …, s5], sII = [s6, s7, s8, s9], etc. The IF of input labels sj>0 into partitions sI, sII, sIII, … sXVII was carried out according to expert criteria. In so doing, we grouped together labels of the same type or category of data, i.e., sI = Genetic and age group labels, sII = Disease condition labels,sIII = Microbiology lab data labels, etc. Please, see the codes, names, and values of all the input labels and their partitions in Table 2.(https://github.com/glezdiazh/CFIBRO.PTML/issues/2#issue-2560514774). 



In this IF horizontal process, we performed two steps, see Figure 2. Firstly we carried out the IF of one continuous input variable Vki at time vs. one partition of input labels sI, sII, …., or sIII.  This process leads to the calculation of the first order PTOs with the form of multi-condition deviations ∆Vki(sj). The calculation of these PTOS is explained above. As we have Nvars = 36 input continuous variables (Vki) and Nlabels = 39 input labeling variables (sj>0) grouped into 7 partitions sj we could calculate theoretically a total of Ndev = 36·7 = 252 operators ∆Vki(sj). However, we used similar expert criteria to regroup all continuous input variables into partitions of continuous variables cj. Each one of these partitions cj is constructed as an IF or regrouping of different input continuous variables Vki, i.e., cI = [v1, v2, v3, …, v6], cII = [v7, v8, v9], etc. The IF of input continuous variables into partitions cI, cII, cIII, … cVII was carried out according to similar expert criteria than those used for the input labels sj>0.In so doing, we grouped together labels of the same type or category of data, i.e., sI = Genetic and age group, sII = Disease condition labels, sIII = Microbiology lab data labels, etc. After this, we were able to calculate the PTOs of second order in the form of Euclidean Distances ǁ∆Vk(sjǁcj. These parameters measure the distance between the values Vki of the ith patient with respect to all patients we the same values of sj. Please, see the codes, names, and values of all the input variables and their partitions in (Table 1 and Table 2).

# IF vertical process and outputs preprocessing
The vertical IF process is illustrated also in Figure 2. In the original dataset compiled with have a total of Noutput = 4 outcome values by patient and interview. These output variables have the values vij and the labels or names s0= FEV1, FVC%, HD(dd) and ATBiv days. In the case we treat each one of these variables as a column we shall have 4 objective variables. As consequence, we will need to train 4 different models (one model for each objective variable) and/or use multi-objective techniques allowing more than one output variable. One alternative is to carry out an IF process grouping all the 4 output variables into only one by means of a vertical rearrangement all these values into on column. In so doing, we need to use an output labeling variable s0 to indicate to what variable belongs each outcome value vij. This allow the IFPTML algorithm to process multiple output variables at the same time by training multi-output models with a single equation (Santiago et al., 2022). Once we assembled all outcome values vij into one objective variable (column) we proceeded to the preprocessing of the values in order to put all of them into the same scale. In this work we transformed the original values vobsij into the objective function with values f(vij)obj = 1 => patient with moderate to severe disease symptoms or f(vij)obj = 0 => patient with mild disease symptoms. The values of the objective function are calculated as follow:









