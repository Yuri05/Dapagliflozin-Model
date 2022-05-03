### 2.3.1 Absorption

Studies including oral applications of dapagliflozin used for model building applied either a capsule or immediate release tablets. They all demonstrated rapid and extensive absorption. The availability of dense data during absorption, data covering a broad range of doses (from 2.5 up to 500 mg), and intravenous pharmacokinetic data ([Boulton 2013](#5-references)) allowed the identification of the *in vivo* intestinal permeability and an effective *in vivo* solubility in this PBPK model (see also [Section 2.3.4](#234-automated-parameter-identification)).

During model building, two different "data scenarios" regarding mass balance information were tested:

**Scenario 1**: The measured fraction excreted to feces as unchanged drug of approx. 19% resulted from incomplete absorption (assuming f<sub>a</sub>  ~ 0.81).

**Scenario 2**:  The measured fraction excretion to feces of unchanged dapagliflozin resulted from originally glucuronidated metabolites that underwent biliary excretion and subsequent degradation to dapagliflozin by bacterial glucuronidases in feces (assuming f<sub>a</sub> ~ 1). The cleavage of hepatobiliary secreted glucuronides to the aglycone (e.g. parent drug) by beta-glucuronidases in the colon was reported previously ([Blaut 2013](#5-references), [Molly 1993](#5-references), [Possemiers 2004](#5-references), [Sakamoto 2002](#5-references)). 

Scenario 1 did not allow to find a good description of the pharmacokinetic data. Thus, scenario 2 was used during further model building. Note that this increased the fraction metabolized via UGT1A9 and UGT2B7.

The dissolution of the tablets from Chang *et al.* ([Chang 2015](#5-references)) - referenced as individual component (IC) tablets - were implemented via an empirical Weibull dissolution tablet. The respective parameters were identified via manual sensitivity analysis.

### 2.3.2 Distribution

Dapagliflozin is moderately protein bound (91 %) in plasma ([Kasichayanula 2014](#5-references)). This value was used in this PBPK model. It was assumed that the major binding partner is albumin.

An important parameter influencing the resulting volume of distribution is lipophilicty. The reported experimental logP value of 2.7 ([DrugBank DB06292](#5-references)) served as a starting value. Finally, the model parameters `Lipophilicity` and `logP (veg.oil/water)` were optimized to match best clinical data (see also [Section 2.3.4](#234-automated-parameter-identification)).

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim, observed clinical data was best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`. The specific organ permeability was also optimized to match best clinical data (see also [Section 2.3.4](#234-automated-parameter-identification)).

The reported blood to plasma ratio of 0.88 ([Obermeier 2009](#5-references)) was fixed in the model.

### 2.3.3 Metabolism and Elimination

As previously described in [Section 2.2.2](#222-clinical-data),  mass balance data ([Kasichayanula 2008](#5-references), [Obermeier 2009](#5-references), [Kasichayanula 2014](#5-references)) indicated that UGT1A9 is predominatly responsible for the metabolism of dapagliflozin to dapagliflozin-3-O-glucuronide. A minor fraction is metabolized via UGT2B7 to dapagliflozin-2-O-glucuronide and via oxidative cytochrome-P450 enzymes.

In summary, three metabolic first order routes were implement into the model:

* UGT1A9-specific clearance
* UGT2B7-specific clearance
* an unspecific hepatic oxidative clearance ("Hepatic-CYP")
  (The hypothetical lumped Hepatic-CYP enzyme was assumed to be expressed only in the liver with a reference concentration of 1 µmol/L.)

Additionally, a renal clearance (assumed to be mainly driven by glomerular filtration) was implemented.

This clearance and excretion pathways were quantified during parameter optimization to best match clinical data (see also [Section 2.2.2](#222-clinical-data), [Section 2.3.1](#231-absorption), and [Section 2.3.4](#234-automated-parameter-identification)).

### 2.3.4 Automated Parameter Identification

This is the result of the final parameter identification.

| Model Parameter                    | Optimized Value | Unit       |
| ---------------------------------- | --------------- | ---------- |
| `Lipophilicity`                    | 2.672           | Log Units  |
| `logP (veg.oil/water)`             | 2.083           | Log Units  |
| `Permeability`                     | 3.75E-04        | cm/min     |
| `Specific intestinal permeability` | 3.97E-05        | cm/min     |
| `Solubility at reference pH`       | 0.221           | mg/ml      |
| `CLspec/[Enzyme]` (UGT1A9)         | 0.399           | l/µmol/min |
| `CLspec/[Enzyme]` (UGT2B7)         | 6.60E-03        | l/µmol/min |
| `CLspec/[Enzyme]` (Hepatic-CYP)    | 0.143           | l/µmol/min |
| `GFR fraction`                     | 0.79            |            |
| `Blood/Plasma concentration ratio` | 0.88 FIXED      |            |

