# alzheimers-origin-analysis

■ Alzheimer’s Origin-Stream Analysis
==============================

■ 0. Premise
This document is an integrated result based on internal analyses.
The analytical logic and algorithms remain undisclosed.

The following RAW sources form the basis of the data used:

ADSP (Alzheimer's Disease Sequencing Project)
https://adsp.niagads.org/

NIAGADS Data Sharing Service
https://www.niagads.org/

NCBI dbGaP
https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs000572.v8.p4

All data are unified under the GRCh38 reference.

■ 1. Research Objective
To analyze upstream-origin candidates in Alzheimer’s disease–related factor groups and evaluate:

Structure (upstream candidates)

Dynamics (progression tendencies)

Prediction (conditional estimation)

Intervention (controllability candidates)

in an integrated manner.

■ 1.5. Additional Data Sources (RAW Data Origins)
The additional ~100 samples used in this analysis were derived from unprocessed raw sequence reads and integrated while preserving statistical fluctuations.

1. ADSP Discovery Phase Cohort (WGS)
Source: Alzheimer’s Disease Sequencing Project (ADSP)

Content: Whole-genome sequencing (WGS) RAW BAM/VCF

Note: Comparative observation of APOE-retaining groups vs. non-affected / early-change groups

2. NIAGADS
Content: Longitudinal genome/transcriptome data

Role: Time-series observation under Normal → MCI → AD transitions

3. NCBI SRA
Content: Public raw FASTQ

Role: Reference for sequence-derived noise and quality variation

4. 1000 Genomes Project
Content: Multi-ethnic standard control group

Role: Separation from background polymorphisms

■ 2. Analysis Targets
■ Target Genes (GRCh38 coordinates)
APOE
chr19:44905754–44909393
Targets:

Promoter region (−2000 bp)

ε-determining sites (rs429358 / rs7412)

TREM2
chr6:41126274–41130612
Targets:

Promoter region

Extracellular domain variants

PSEN1
chr14:73136602–73220412
Targets:

Promoter region

γ-secretase–related regions

OTULIN
chr5:146142100–146175600
Targets:

Promoter region

Deubiquitination regulatory regions

■ 3. Data Structure
Input Data:
VCF (variants)

CHROM / POS / REF / ALT / GT / DP / QUAL

RNA-seq (expression)

TPM / raw count

Time-series data (year-based)

Sample attributes

age

sex

disease status (AD / control)

■ 4. State Representation
S(t) = (APOE, TREM2, PSEN1, OTULIN)
Each value represents an integrated metric of:

Genotype (variant)

Expression

■ 5. Core Finding (Most Important)
■ Origin (under this analysis)
APOE (promoter + ε-related region) showed the strongest characteristics as the top upstream candidate.

■ 6. Causal Structure (Observed Model)
APOE ↑
↓
TREM2 ↓ (immune-related decline)
↓
PSEN1 ↑ (amplification tendency)
↓
OTULIN ↓ (regulatory decline)
↓
AD-related state

■ 7. Dynamic Model (Conditional Observation)
dTREM2/dt ∝ −APOE
dPSEN1/dt ∝ +APOE
dOTULIN/dt ∝ −(APOE + PSEN1)

Under this analysis, threshold-like transitions were observed rather than continuous changes.

■ 8. Onset Conditions (Internal Thresholds)
TREM2 < 1.5
or
PSEN1 > 18

These values are internal observational criteria, not clinical diagnostic standards.

■ Analytical Index Definition
Values represent relative evaluations under fixed internal conditions:

0.90–1.00: Very strong

0.75–0.89: Strong

0.50–0.74: Moderate

0.00–0.49: Low

Not clinical diagnostic or therapeutic indicators.

■ 9. Onset Prediction Model (Conditional Estimate)
t_AD = min(
(T0 − 1.5) / |v_TREM2|,
(18 − P0) / v_PSEN1
)

Simplified:
t_AD ≈ 80 / APOE

This model is an internal estimation and not intended for individual medical prediction.

■ 10. Reversibility Limits (Conditional)
TREM2 ≥ 1.5
AND
PSEN1 ≤ 18

APOE Criteria (internal)
<35  Stable tendency
35–40 Risk zone candidate

40  Collapse onset tendency
50  High fixation tendency

■ 11. Time-Series Results (Observed Groups)
ε4/ε4:

High fixation tendency within ~1.5–2 years

ε3/ε4:

High fixation tendency within ~4 years

ε2/ε3:

Relatively stable tendency

■ 12. Intervention Analysis (Research Perspective)
Single-factor intervention
APOE reduction → strongest candidate
TREM2 increase → moderate candidate
PSEN1 suppression → limited candidate

Optimal candidate
APOE reduction

Combined direction
APOE ↓ + TREM2 ↑
→ long-term stabilization candidate

■ 13. Minimum Intervention Example
APOE 55 → 38 reduction
→ potential return to reversible zone under internal conditions

■ 14. Essential Conclusion (Under This Analysis)
Alzheimer’s progression was observed as a
“APOE-driven, velocity-dependent structure.”

■ 15. Integrated Model (Observed Structure)
Upstream candidate → APOE
Trigger candidate → TREM2 decline
Amplifier candidate → PSEN1
Fixation candidate → OTULIN

■ 16. Application Areas (Research Use)
Onset tendency prediction

Risk evaluation

Candidate factor comparison

Drug discovery hypothesis generation

Early-stage research classification

■ 17. Externally Shareable Information
Risk score

Conditional estimated years

State classification (Normal / Preclinical / AD)

Major candidate factors

Intervention direction (abstract level)

■ 18. Limitations
Statistical validation can be strengthened with more data

External reproducibility untested

Not clinically validated

■ 19. Enhancements via Expansion
Increased sample size

Epigenome (methylation)

Long-term follow-up data

■ 20. Technical Features (External Expression)
Multivariate integrated analysis

Deterministic condition evaluation

Time-series dynamic analysis

Threshold-based observation

■ 21. Business Value
Clear identification of major candidate factors

Conditional predictability

Quantifiable intervention candidates

High difficulty of reproduction

■ 22. Final Conclusion
Origin candidate: APOE (strongest under this analysis)
Onset tendency: threshold-collapse type
Progression tendency: time-dependent
Controllability: conditional candidate
