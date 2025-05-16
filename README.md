# kenya-stem-digital-efficacy
# Analysis of Teachers' Efficacy in Using Digital Resources for STEM Subjects in Kenyan Schools


## 1. Project Overview

This repository contains the data, analysis scripts, and findings for the "Situational Analysis on Teachers’ Efficacy in Using Digital Resources for Effective Learning of STEM Subjects in Kenyan Schools." The project, based on research outlined in the associated synopsis document (see `docs/` or `reports/`), aims to assess how effectively teachers in Kenyan Junior and Secondary schools are utilizing digital resources for STEM (Science, Technology, Engineering, and Mathematics) education.

The primary goals are to understand the current landscape, identify challenges, and provide actionable insights for stakeholders such as CEMASTEA (Centre for Mathematics, Science and Technology Education in Africa) and the Ministry of Education, Kenya.

### Research Objectives:

**General Objective:**
* To assess the teachers’ efficacy on the use of digital resources for learning STEM subjects in Kenyan schools.

**Specific Objectives:**
1.  To investigate the relationship between teacher training (TPD) in STEM and their ability to effectively use digital resources.
2.  To establish the influence of the use of digital resources on the teacher's instructional practices in STEM subjects.
3.  To establish teachers’ awareness on the available digital resources for STEM subjects.
4.  To assess the extent of support provided to teachers for adopting digital resources in teaching STEM subjects.

**Keywords:** STEM Education, Digital Resources, Teacher Efficacy, Kenya, Educational Technology, Teacher Training, Instructional Practices, CEMASTEA, CBC Kenya, Data Analysis, Situational Analysis.

---

## 2. Repository Structure

.├── data/│   ├── raw/                  # Original, immutable CSV data files (as provided by user)│   │   ├── FGD-JS Demographic.csv│   │   ├── FGD-JS Data.csv│   │   ├── FGD-Sec.xlsx - Sheet1.csv│   │   ├── HoI-JS.xlsx - Data.csv│   │   ├── HoI-JS.xlsx - Summary.csv│   │   ├── HoI - Sec.xlsx - Data.csv│   │   ├── HoI - Sec.xlsx - Summary.csv│   │   ├── LO - JS .xlsx - Raw Data.csv│   │   ├── LO - JS .xlsx - %Summary.csv│   │   ├── LO - JS .xlsx - Analysis.csv│   │   ├── LO - JS .xlsx - Demographic.csv│   │   ├── LO - JS .xlsx - Summary.csv│   │   ├── LO - Sec.xlsx - Raw Data.csv│   │   ├── LO - Sec.xlsx - % summary.csv│   │   ├── LO - Sec.xlsx - Summary.csv│   │   ├── Teachers' Questionnaire-JS.xlsx - Data.csv│   │   ├── Teachers' Questionnaire-JS.xlsx - Summary.csv│   │   ├── Teachers' Questionnaire-JS.xlsx - Trained.csv│   │   ├── Teachers' Questionnaire-JS.xlsx - Untrained.csv│   │   ├── Teacher Questionnaire-Sec Schl.xlsx - Sheet1.csv│   │   ├── Teacher Questionnaire-Sec Schl.xlsx - Summary _ Demo.csv│   │   ├── Teacher Questionnaire-Sec Schl.xlsx - Item-Analysis.csv│   │   └── Teacher Questionnaire-Sec Schl.xlsx - Freq & Percentages.csv│   ├── processed/            # Cleaned, merged, or transformed data files ready for analysis│   │   └── (e.g., combined_teacher_questionnaire.csv, thematic_analysis_fgd.xlsx)│   └── data_dictionaries/    # (Optional) Files explaining variables, codes, etc.├── notebooks/                # Jupyter notebooks or R scripts for data analysis│   ├── 00_data_loading_and_initial_exploration.ipynb│   ├── 01_data_cleaning_and_preparation.ipynb│   ├── 02_descriptive_stats_demographics.ipynb│   ├── 03_analysis_objective1_training_efficacy.ipynb│   ├── 04_analysis_objective2_instructional_practices.ipynb│   ├── 05_analysis_objective3_resource_awareness.ipynb│   ├── 06_analysis_objective4_support_systems.ipynb│   └── 07_qualitative_thematic_analysis.ipynb├── reports/                  # Final reports, presentations, and the research synopsis│   ├── Research_Synopsis_Teachers_Efficacy_Digital_Resources.docx (or PDF version)│   ├── Final_Analysis_Report.pdf│   └── Stakeholder_Presentation.pptx├── visualizations/           # Scripts to generate visualizations or exported static images/charts│   ├── static_charts/│   │   ├── obj1_training_vs_efficacy.png│   │   ├── obj2_digital_tool_usage_frequency.png│   │   ├── obj3_resource_awareness_levels.png│   │   ├── obj4_support_satisfaction_levels.png│   │   └── ... (other key charts)│   └── (e.g., tableau_dashboard_screenshots/ if applicable)├── src/                      # (Optional) Custom Python/R modules or utility scripts│   └── data_utils.py├── README.md                 # This file: project overview, setup, and navigation├── requirements.txt          # Python dependencies (pip freeze > requirements.txt)└── .gitignore                # Specifies intentionally untracked files that Git should ignore
---

## 3. Data Sources

The analysis is based on data collected from a pilot study conducted in 20 of the 47 counties in Kenya, representing all eight regions. Data was collected using:

* **Head of Institution (HoI) Interview Guide:** Perspectives from school leadership on policies, resource availability, and institutional support. (Files: `HoI-*.csv`)
* **Teacher Questionnaire (TQ):** Quantitative and qualitative data from teachers on demographics, training (TPD), self-efficacy, awareness of digital resources, instructional practices, and perceived support. (Files: `Teacher*.csv`, `Teachers'*.csv`)
* **Learner Focus Group Discussion (FGD) Guide:** Qualitative insights from learners regarding their experiences with teachers' use of digital resources and the learning environment. (Files: `FGD-*.csv`)
* **Lesson Observation (LO) Guide:** Observational data on actual classroom practices, including the integration and use of digital resources by teachers. (Files: `LO - *.csv`)

All raw data files are located in the `data/raw/` directory. The research synopsis document ("A synopsis on Data Analysis and report writing-Situational Analysis on teachers' Efficacy on the use of digital resources.docx"), which provides further context on data collection and initial challenges, can be found in the `reports/` directory.

**Key Data Limitations (as noted in the synopsis):**
* The pilot study data was found unsuitable for complex inferential statistics like regression modeling. Therefore, the analysis primarily focuses on **descriptive statistics** (frequencies, percentages, means) and **thematic analysis** of qualitative data.
* Triangulation of data, especially between self-reported teacher questionnaire data and lesson observation data, presented challenges due to potential biases (self-reporting bias, observer bias).

---

## 4. Methodology

The project follows the Cross-Industry Standard Process for Data Mining (CRISP-DM) framework, adapted for this research context:

1.  **Business/Research Understanding:** Defined by the research synopsis, focusing on the general and specific objectives.
2.  **Data Understanding:** Initial exploration of each dataset to understand its structure, variables, and quality. (See `notebooks/00_data_loading_and_initial_exploration.ipynb`)
3.  **Data Preparation:** Cleaning missing values, handling inconsistencies, transforming data types, and structuring data for analysis. Qualitative data from FGDs and open-ended questions were prepared for thematic analysis. (See `notebooks/01_data_cleaning_and_preparation.ipynb`)
4.  **Modeling (Analysis):**
    * **Quantitative Analysis:** Descriptive statistics (frequencies, percentages, means, cross-tabulations) were generated to address the research objectives. Visualizations include bar charts, pie charts, and tables.
    * **Qualitative Analysis:** Thematic analysis was employed for FGD data and open-ended responses from questionnaires to identify key themes, patterns, and illustrative quotes. The synopsis notes that AI was used to assist in generating inductive themes, which did not deviate much from a priori coding.
    (Analysis notebooks: `notebooks/02_*` to `notebooks/07_*`)
5.  **Evaluation:** Findings were reviewed against the research objectives. Limitations of the data and analysis were considered and documented.
6.  **Deployment (Reporting):** Results are summarized in this README, detailed in the final report, and visualized for presentations (see `reports/` and `visualizations/`).

---

## 5. Key Findings & Visualizations

This section will be populated with key findings and illustrative visualizations as the analysis progresses. Visualizations will be stored in `visualizations/static_charts/`.

*(For each objective, provide a concise summary of the findings and embed 1-2 key visualizations. Use Markdown image embedding: `![Alt text for image](path/to/your/image.png)`)*

### 5.1 Objective 1: Teacher Training (TPD) and Ability to Use Digital Resources
* *Summary of findings on the correlation between TPD participation, type/duration of training, and teachers' self-reported ability or efficacy in using digital tools.*
* **Placeholder Visualization:**
    * `![TPD Impact on Efficacy](visualizations/static_charts/obj1_training_vs_efficacy.png)`
    * *Caption: e.g., "Figure 1: Teacher-Reported Efficacy in Using Digital Tools by TPD Training Status (Junior vs. Secondary Schools)"*

### 5.2 Objective 2: Influence of Digital Resources on Instructional Practices
* *Summary of how teachers report digital resources influencing their teaching methods, and findings from lesson observations and FGDs on observed/perceived changes.*
* **Placeholder Visualization:**
    * `![Digital Tool Usage](visualizations/static_charts/obj2_digital_tool_usage_frequency.png)`
    * *Caption: e.g., "Figure 2: Frequency of Use for Common Digital STEM Resources (Teacher Self-Report vs. Lesson Observation)"*

### 5.3 Objective 3: Teachers’ Awareness of Available Digital Resources
* *Summary of teachers' awareness levels for different types of STEM-related digital resources and platforms.*
* **Placeholder Visualization:**
    * `![Resource Awareness](visualizations/static_charts/obj3_resource_awareness_levels.png)`
    * *Caption: e.g., "Figure 3: Teacher Awareness Levels for Key Digital STEM Resources"*

### 5.4 Objective 4: Support Provided for Adopting Digital Resources
* *Summary of the types and extent of support (institutional, technical, peer, policy) teachers receive and perceive as necessary for effective digital resource integration.*
* **Placeholder Visualization:**
    * `![Support Systems](visualizations/static_charts/obj4_support_satisfaction_levels.png)`
    * *Caption: e.g., "Figure 4: Teacher Satisfaction with Available Support for Digital Resource Use"*

---

## 6. Tools and Technologies Used

* **Programming Languages:** Python 3.x (primarily)
* **Key Python Libraries:**
    * Pandas: Data manipulation and analysis.
    * NumPy: Numerical operations.
    * Matplotlib & Seaborn: Data visualization.
    * SciPy: Statistical analysis (for descriptive stats).
    * NLTK / spaCy (optional, for text processing in qualitative analysis).
    * JupyterLab / Jupyter Notebook: Interactive development and analysis.
* **Qualitative Data Analysis:** [Mention specific software if used, e.g., NVivo, ATLAS.ti, or methods if manual/Python-based] (Synopsis mentions AI-assisted thematic analysis).
* **Visualization (beyond Python):** Tableau (if used for dashboards - link to public dashboard if available).
* **Version Control:** Git & GitHub.

---

## 7. How to Use This Repository

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YourGitHubUsername]/kenya-stem-teacher-digital-efficacy.git
    cd kenya-stem-teacher-digital-efficacy
    ```

2.  **Set up the Python environment:**
    It is recommended to use a virtual environment.
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
    Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
    *(Ensure you create a `requirements.txt` file by running `pip freeze > requirements.txt` in your activated virtual environment after installing all necessary packages.)*

3.  **Explore the notebooks:**
    Navigate to the `notebooks/` directory and run Jupyter Lab or Jupyter Notebook:
    ```bash
    jupyter lab
    ```
    Open the notebooks sequentially to follow the analysis workflow.

4.  **Access Data and Reports:**
    * Raw data is in `data/raw/`.
    * Processed data (if any generated) will be in `data/processed/`.
    * Final reports and the synopsis are in `reports/`.
    * Static visualizations are in `visualizations/static_charts/`.

---

## 8. Summary of Conclusions & Recommendations

*(This section will be populated upon completion of the analysis. It will provide a high-level summary of the overall conclusions and key recommendations for stakeholders. For detailed conclusions and recommendations, refer to the `Final_Analysis_Report.pdf` in the `reports/` directory.)*

**Example Placeholder Conclusion:**
* *Overall, teacher efficacy in using digital resources in Kenyan STEM education is [emerging/moderate/varied], significantly influenced by [key factor 1, e.g., targeted TPD] and [key factor 2, e.g., consistent institutional support]...*

**Example Placeholder Recommendations:**
1.  **For CEMASTEA/MoE:** *Develop and scale TPD programs focusing on pedagogical integration of specific STEM digital tools, rather than generic ICT skills...*
2.  **For School Administrators:** *Establish clear school-level policies and dedicated budgets for acquiring and maintaining digital resources, alongside providing protected time for teacher collaboration and peer support...*
3.  **For Future Research:** *Conduct a larger-scale study with robust data collection instruments designed to support inferential statistical analysis and more effective triangulation...* (as per synopsis)

---

## 9. Contributors

* [Your Name/Team Name] - Lead Data Analyst
* [If applicable, list other team members or acknowledge the original research team/CEMASTEA]

---

## 10. License

* Specify the license under which this project is shared (e.g., MIT, Creative Commons, Apache 2.0). If the data has specific sharing restrictions, note them here.
* Example: `This project is licensed under the MIT License - see the LICENSE.md file for details.` (You would then create a `LICENSE.md` file).
* If no specific open-source license is chosen, you might state: "All rights reserved by [Your Name/Organization] unless otherwise specified."

---

