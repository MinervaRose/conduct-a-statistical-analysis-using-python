# Conduct a Statistical Analysis Using Python — Space Mission Launches (Udacity Capstone section 3)

## Project Description
This project performs a complete statistical analysis of historical space mission launches, framed through an **aerospace launch risk analysis** lens. Using a real-world Kaggle dataset, I build a reproducible workflow that screens data quality, summarizes key variables, visualizes patterns, and performs statistical inference to test whether mission outcomes are associated with launch cost.

This project intentionally focuses on **statistical reasoning (not machine learning)** as a foundation for later ML, deep learning, and agentic systems work.

**Dataset used:** Space Mission Launches (Kaggle)  
https://www.kaggle.com/datasets/sefercanapaydn/mission-launches

---

## What I Built
A complete statistical analysis workflow that includes:

- **Data ingestion** from CSV (reproducible pathing for local or Colab use)
- **Initial Data Analysis (IDA) screening**
  - data types validation
  - missing data quantification (especially launch pricing)
  - removal of non-analytical index artifacts
- **Descriptive statistics**
  - numeric summaries for launch price
  - categorical counts for mission outcomes and organizations
- **Five visualizations** (each with titles, axis labels, and notebook captions)
  1. Launch price distribution (histogram)
  2. Launch price by mission outcome (boxplot)
  3. Mission outcome frequencies (count plot)
  4. Top organizations by mission count (bar chart)
  5. Launch price over time (scatter plot)
- **Hypothesis testing**
  - Welch’s two-sample *t* test comparing launch prices for **Success vs Failure**
  - clearly stated null/alternative hypotheses
  - test statistic and p-value reported
- A written **Statistical Analysis Report (PDF)** with APA citations, limitations, and a non-technical interpretation

---

## Analytical Question (Launch Risk Angle)
**Do successful missions have a different average launch price than failed missions?**

This question connects **mission reliability (risk)** with **economic exposure**, which is a practical concern in aerospace operations and monitoring systems.

---

## How to Run

### 1) Install dependencies
```bash
pip install -r requirements.txt
```

The requirements file was generated using:
```pip freeze > requirements.txt
```
### 2) Run the notebook

* Clone or download this repository
* Open analysis.ipynb in Jupyter Notebook or Google Colab
* Run all cells from top to bottom

The notebook is designed to execute without hidden state and reproduce all outputs.

---

## Reproducibility Notes (IDA-Informed Workflow)

This project emphasizes reproducible analysis practices:

* Data screening is performed before inference (types, missingness, validity checks)
* The notebook runs top-to-bottom without manual intervention
* Outputs (figures + test results) reproduce consistently
* requirements.txt captures the environment for reruns

The workflow design aligns with recommendations that systematic initial data analysis (IDA) and clear reporting strengthen reproducibility and reduce ad-hoc analytic decisions.

---

## Limitations and Potential Bias (Summary)

Missing launch prices: Most missions do not contain pricing data, so cost-based inference uses a reduced subset of the dataset.

Outcome imbalance: Successes vastly outnumber failures, which limits the failure sample size and can increase uncertainty for failure-related estimates.

Observational data: Associations observed here should not be interpreted as causal. Confounders may include mission type, era, vehicle class, and reporting practices.

These limitations are discussed in detail in the PDF report.

---

## Repository Structure

📓 analysis.ipynb
📄 Statistical_Analysis_Report.pdf
📄 requirements.txt
📦 mission_launches.csv
📘 README.md

---

## References
* Lusa, L., Proust-Lima, C., Schmidt, C. O., Lee, K. J., le Cessie, S., Baillie, M., … Huebner, M. (2024). Initial data analysis for longitudinal studies to build a solid foundation for reproducible analysis. PLOS ONE, 19(5), e0295726. https://doi.org/10.1371/journal.pone.0295726

* Lee, K. J., Tilling, K. M., Cornish, R. P., Little, R. J. A., Bell, M. L., Goetghebeur, E., … Carpenter, J. R. (2021). Framework for the treatment and reporting of missing data in observational studies: The TARMOS framework. Journal of Clinical Epidemiology, 134, 79–88. https://doi.org/10.1016/j.jclinepi.2021.01.008

* Ruxton, G. D. (2006). The unequal variance t-test is an underused alternative to Student’s t-test and the Mann–Whitney U test. Behavioral Ecology, 17(4), 688–690. https://doi.org/10.1093/beheco/ark016

* Sefercanapaydn. (n.d.). Mission launches [Data set]. Kaggle.
https://www.kaggle.com/datasets/sefercanapaydn/mission-launches


