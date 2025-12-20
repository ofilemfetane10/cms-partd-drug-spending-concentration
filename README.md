# Concentration in Medicare Part D Drug Spending

This repository analyses prescription drug spending under Medicare Part D using publicly available data from the Centers for Medicare & Medicaid Services (CMS).

The focus of the analysis is **market concentration**: how total Medicare Part D spending is distributed across individual drugs, and the extent to which a small number of products dominate overall expenditure.

---

## Research Focus

Medicare Part D is often described as a competitive prescription drug market. However, aggregate spending patterns can reveal whether competition meaningfully distributes costs or whether spending is concentrated in a small subset of drugs.

This project addresses the following questions:

- How concentrated is Medicare Part D drug spending?
- How many drugs account for a large share of total spending?
- What does the distribution of spending suggest about market power within Part D?

The analysis is structural and descriptive, focusing on spending dominance rather than clinical outcomes or utilisation behavior.

---

## Data Source

The analysis uses the **CMS Medicare Quarterly Part D Spending by Drug** dataset.

Although CMS releases data on a quarterly basis, this project focuses on the **most recent complete annual spending period available at the time of analysis (2024, Q1–Q4)** to avoid distortions from partial-year reporting.

Each record includes:
- Total Medicare Part D spending per drug
- Total beneficiaries and claims
- Average spending per beneficiary and per claim
- Manufacturer aggregation

To prevent double counting, the analysis uses drug-level **“Overall”** records, which aggregate spending across manufacturers.

---

## Methodology

The analytical approach includes:

- Cleaning and normalising CMS drug spending fields
- Filtering to drug-level aggregated records
- Ranking drugs by total Medicare Part D spending
- Calculating spending shares and cumulative concentration
- Visualising concentration using a cumulative spending curve

All analysis was conducted in Python using Pandas and Matplotlib.

---

## Key Findings

- Medicare Part D spending is **highly concentrated**.
- Approximately **eight drugs account for around half of total Part D spending**.
- A small group of high-cost, high-dependence drugs dominates program expenditure.
- The spending distribution exhibits a long tail, with hundreds of drugs accounting for the remaining share.

These patterns indicate strong market power among a limited number of pharmaceutical products.

---

## Visual Output

The repository includes a single visualisation:

- **Cumulative concentration curve** showing the share of total Medicare Part D spending captured as drugs are ranked by total expenditure.

This visual demonstrates how quickly spending accumulates among the highest-ranked drugs.

---

## Limitations

- The analysis uses aggregated annual spending data and does not examine quarter-to-quarter variation.
- Manufacturer-level pricing strategies are not analysed separately.
- Clinical effectiveness, outcomes, and cost-effectiveness are outside the scope of this project.

The findings are descriptive and intended to inform policy and market-structure discussions.

---

## Disclaimer

This analysis is based on a ranked extract retrieved via the CMS Open Data API. While it does not constitute a full census of all records, the approach is sufficient for identifying dominant patterns, structural concentration, and distributional dynamics within the dataset.

---

## Related Work

This repository is part of a broader research series examining structural power and concentration in U.S. healthcare, including:

- Hospital enrolment structure
- Hospital ownership and governance
- Skilled nursing facility enrolments
- Ownership concentration in long-term care

Each repository addresses a distinct dataset and analytical question.

---

## Code and Reproducibility

The full analysis is contained in a single Jupyter notebook and can be reproduced using standard Python data science libraries.

---

## Author

**Ofile Seneo Mfetane**  
Business Intelligence & Data Analytics
