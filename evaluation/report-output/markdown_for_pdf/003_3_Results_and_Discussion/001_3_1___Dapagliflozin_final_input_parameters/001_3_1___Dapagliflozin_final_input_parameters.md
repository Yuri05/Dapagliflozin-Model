## 3.1   Dapagliflozin final input parameters
The compound parameter values of the final dapagliflozin PBPK model are illustrated below.




# Compound: Dapagliflozin

## Parameters

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
## Calculation methods

Name                    | Value               |
----------------------- | ------------------- |
Partition coefficients  | Rodgers and Rowland |
Cellular permeabilities | PK-Sim Standard     |
## Processes

### Metabolizing Enzyme: UGT1A9-Optimized

Molecule: UGT1A9
Metabolite: Dapagliflozin-3-O-glucuronide
#### Parameters

Name                 | Value                  | Value Origin                                                                                               |
-------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l               |                                                                                                            |
Specific clearance   | 0 1/min                |                                                                                                            |
CLspec/[Enzyme]      | 0.402175146 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
### Metabolizing Enzyme: UGT2B7-Optimized

Molecule: UGT2B7
Metabolite: Dapagliflozin-2-O-glucuronide
#### Parameters

Name                 | Value                      | Value Origin                                                                                               |
-------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l                   |                                                                                                            |
Specific clearance   | 0 1/min                    |                                                                                                            |
CLspec/[Enzyme]      | 0.0072288071857 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
### Systemic Process: Glomerular Filtration-assumed

Species: Human
#### Parameters

Name         |        Value | Value Origin                                                                                               |
------------ | ------------:| ---------------------------------------------------------------------------------------------------------- |
GFR fraction | 0.8944188606 | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |
### Metabolizing Enzyme: Hepatic-CYP-Optimized

Molecule: Hepatic-CYP
#### Parameters

Name                 | Value                   | Value Origin                                                                                               |
-------------------- | ----------------------- | ---------------------------------------------------------------------------------------------------------- |
Enzyme concentration | 1 µmol/l                |                                                                                                            |
Specific clearance   | 0 1/min                 |                                                                                                            |
CLspec/[Enzyme]      | 0.1397810065 l/µmol/min | Parameter Identification-Parameter Identification-Value updated from 'PI full  (perm)' on 2019-08-06 14:46 |

# Formulation: IR tablet

Type: Weibull
## Parameters

Name                             | Value  | Value Origin |
-------------------------------- | ------ | ------------: |
Dissolution time (50% dissolved) | 30 min |              |
Lag time                         | 0 min  |              |
Dissolution shape                | 0.6    |              |
Use as suspension                | Yes    |              |

# Formulation: Solution

Type: Dissolved

