<h1> Building and evaluation of a PBPK model for dapagliflozin in adults</h1>


<div style="page-break-after: always;"></div>
[toc]
# 1 Introduction
The presented model building and evaluation report evaluates the performance of PBPK model for dapagliflozin in adults.

Dapagliflozin, 

The dapagliflozin model is a whole-body PBPK model, allowing for dynamic translation ....

...reliable predictions of dapagliflozin PBPK adults during model-informed drug development. The presented dapagliflozin PBPK model as well as the respective evaluation plan and PBPK report are provided open-source and transparently documented (https://github.com/sfrechen/Dapagliflozin-Model).


# 2 Methods


## 2.1 Modeling strategy
The general concept of building a PBPK model has previously been described by Kuepfer et al. ([Kuepfer 2016](# 5 References)) Regarding the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in adults was gathered from the literature and has been previously published ([PK-Sim Ontogeny Database Version 7.3](# References)). The information was incorporated into PK-Sim® and was used as default values for the simulations in adults.

The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3 ([Schlender 2016](# 5 References)) or otherwise referenced for the specific process.

First, a base mean model was built using data from the single dose escalation study study to find an appropriate structure describing the PK of dapagliflozin plasma. The mean PK model was developed using a typical European individual. Unknown parameters were identified using the Parameter Identification module provided in PK-Sim®. Structural model selection was mainly guided by visual inspection of the resulting description of data and biological plausibility.

Once the appropriate structural model was identified, additional parameters for different formulations were identified. 

A final PBPK model was established and simulations were compared to the reported data to evaluate model appropriateness and to assess model qualification, by means of diagnostics plots and predicted versus observed concentration-time profiles, of which the results support an adequate prediction of the PK in adults.

During model building, uncertainties in data-quality, as well as study differences may cause not being able to adequately describe the PK of all reported clinical study data. 


## 2.2 Data used
### 2.2.1	In vitro / physico-chemical data

A literature search was performed to collect available information on physical chemical properties of dapagliflozin. The obtained information from literature is summarized in the table below, and is used for model building.

| **Parameter**   | **Unit**    | **Dapagliflozin literature** | **Description**                                 |
| :-------------- | ----------- | ---------------------------- | ----------------------------------------------- |
| MW              | g/mol       |                              | Molecular weight                                |
| pKa             |             |                              | Acid dissociation constant                      |
| Solubility (pH) | mg/L        |                              | Solubility                                      |
| logP            |             |                              | Partition coefficient between octanol and water |
| fu              |             |                              | Fraction unbound                                |
|                 | µM          |                              | Michaelis-Menten constant (Km)                  |
|                 | nmol/min/mg |                              | Vmax                                            |
|                 |             |                              |                                                 |
|                 |             |                              |                                                 |

### 2.2.2	Clinical data

A literature search was performed to collect available clinical data on dapagliflozin in adults. 

The following publications were found in adults for model building and evaluation:

| Publication             | Study description |
| :---------------------- | :---------------- |
| [Dummy](# 5 References) | ...               |
|                         |                   |
|                         |                   |
|                         |                   |
|                         |                   |
|                         |                   |


## 2.3 Model parameters and assumptions
### 2.3.1	Absorption



### 2.3.2	Distribution



### 2.3.3	Metabolism and Elimination



# 3 Results and Discussion
The PBPK model **dapagliflozin** was developed with clinical pharmacokinetic data covering ...

## 3.1   Dapagliflozin final input parameters
The compound parameter values of the final dapagliflozin PBPK model are illustrated below.




### Compound: Dapagliflozin

#### Parameters

Name                                             | Value                   | Value Origin                                                                                               | Alternative      | Default |
------------------------------------------------ | ----------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------- | ------- |
Solubility at reference pH                       | 0.2100844168 mg/ml      | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 | Water solubility | True    |
Reference pH                                     | 7                       | Database-DrugBank DB06292                                                                                  | Water solubility | True    |
Lipophilicity                                    | 2.6495139838 Log Units  | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 | Optimized        | True    |
Fraction unbound (plasma, reference value)       | 0.09                    | Publication-Kasichayanula et al. 2014                                                                      | Human            | True    |
Permeability                                     | 0.00041657167125 cm/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 | Optimized        | False   |
Specific intestinal permeability (transcellular) | 3.8347545732E-05 cm/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 | Optimized        | False   |
Cl                                               | 1                       |                                                                                                            |                  |         |
Is small molecule                                | Yes                     |                                                                                                            |                  |         |
Molecular weight                                 | 408.873 g/mol           |                                                                                                            |                  |         |
Plasma protein binding partner                   | Albumin                 |                                                                                                            |                  |         |
#### Calculation methods

Name                    | Value               |
----------------------- | ------------------- |
Partition coefficients  | Rodgers and Rowland |
Cellular permeabilities | PK-Sim Standard     |
#### Processes

##### Metabolizing Enzyme: UGT1A9-Optimized

Molecule: UGT1A9
Metabolite: Dapagliflozin-3-O-glucuronide
###### Parameters

Name                 | Value                  | Value Origin                                                                                               |
-------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l               |                                                                                                            |
Specific clearance   | 0 1/min                |                                                                                                            |
CLspec/[Enzyme]      | 0.402175146 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
##### Metabolizing Enzyme: UGT2B7-Optimized

Molecule: UGT2B7
Metabolite: Dapagliflozin-2-O-glucuronide
###### Parameters

Name                 | Value                      | Value Origin                                                                                               |
-------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l                   |                                                                                                            |
Specific clearance   | 0 1/min                    |                                                                                                            |
CLspec/[Enzyme]      | 0.0072288071857 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
##### Systemic Process: Glomerular Filtration-assumed

Species: Human
###### Parameters

Name         |        Value | Value Origin                                                                                               |
------------ | ------------:| ---------------------------------------------------------------------------------------------------------- |
GFR fraction | 0.8944188606 | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
##### Metabolizing Enzyme: Hepatic-CYP-Optimized

Molecule: Hepatic-CYP
###### Parameters

Name                 | Value                   | Value Origin                                                                                               |
-------------------- | ----------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l                |                                                                                                            |
Specific clearance   | 0 1/min                 |                                                                                                            |
CLspec/[Enzyme]      | 0.1397810065 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |

### Formulation: IR tablet

Type: Weibull
#### Parameters

Name                             | Value  | Value Origin |
-------------------------------- | ------ | ------------: |
Dissolution time (50% dissolved) | 30 min |              |
Lag time                         | 0 min  |              |
Dissolution shape                | 0.6    |              |
Use as suspension                | Yes    |              |

### Formulation: Solution

Type: Dissolved

## 3.2 Dapagliflozin Diagnostics Plots
Below you find the goodness-of-fit visual diagnostic plots for dapagliflozin PBPK model performance (observed versus individually simulated plasma concentration and weighted residuals versus time) of all data used for model building.


![001_plotGOFMergedPredictedVsObserved.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\002_3_2_Dapagliflozin_Diagnostics_Plots\001_plotGOFMergedPredictedVsObserved.png)

GMFE = 1.339394 

![003_plotGOFMergedResidualsOverTime.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\002_3_2_Dapagliflozin_Diagnostics_Plots\003_plotGOFMergedResidualsOverTime.png)

GMFE = 1.339394 

## 3.3: Dapagliflozin Concentration-Time profiles
Simulated versus observed plasma concentration-time profiles of all data are listed below.


![001_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\001_plotTimeProfile.png)

![002_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\002_plotTimeProfile.png)

![003_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\003_plotTimeProfile.png)

![004_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\004_plotTimeProfile.png)

![005_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\005_plotTimeProfile.png)

![006_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\006_plotTimeProfile.png)

![007_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\007_plotTimeProfile.png)

![008_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\008_plotTimeProfile.png)

![009_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\009_plotTimeProfile.png)

![010_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\010_plotTimeProfile.png)

![011_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\011_plotTimeProfile.png)

![012_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\012_plotTimeProfile.png)

![013_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\013_plotTimeProfile.png)

![014_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\014_plotTimeProfile.png)

![015_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\015_plotTimeProfile.png)

![016_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\016_plotTimeProfile.png)

![017_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\017_plotTimeProfile.png)

![018_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\018_plotTimeProfile.png)

![019_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\019_plotTimeProfile.png)

![020_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\020_plotTimeProfile.png)

![021_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\021_plotTimeProfile.png)

![022_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\022_plotTimeProfile.png)

![023_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\023_plotTimeProfile.png)

![024_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\024_plotTimeProfile.png)

![025_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\025_plotTimeProfile.png)

![026_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\026_plotTimeProfile.png)

![027_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\027_plotTimeProfile.png)

![028_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\028_plotTimeProfile.png)

![029_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\029_plotTimeProfile.png)

![030_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\030_plotTimeProfile.png)

![031_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\031_plotTimeProfile.png)

![032_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\032_plotTimeProfile.png)

![033_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\033_plotTimeProfile.png)

![034_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\034_plotTimeProfile.png)

![035_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\035_plotTimeProfile.png)

![036_plotTimeProfile.png](C:\Users\gemuh.AD-BAYER-CNB\Desktop\Markdown\Dapagliflozin\report-output\markdown_for_pdf\003_3_Results_and_Discussion\003_3_3__Dapagliflozin_Concentration-Time_profiles\036_plotTimeProfile.png)

# 4 Conclusion
The final dapagliflozin PBPK model applies metabolism by .... and adequately describes the pharmacokinetics of dapagliflozinin adults receiving SD, MD of dapagliflozin ranging from ...mg, including .....different oral formulations. 

This model could be applied for the investigation of DDI, and translation to special populations such as pediatrics with regard to ... metabolism.

# 5 References
**dummy 2019** Iwamoto M, Wenning LA, Petry AS, Laethem M, De Smet M, Kost JT, Merschman SA, Strohmaier KM, Ramael S, Lasseter KC, Stone JA, Gottesdiener KM, Wagner JA. Safety, tolerability, and pharmacokinetics of raltegravir after single and multiple doses in healthy subjects. Clin Pharmacol Ther. 2008 Feb;83(2):293-9. Epub 2007 Aug 22.
