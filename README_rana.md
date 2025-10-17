## 3. <a name='DatasetContent'></a>Dataset Content

The IBM HR Analytics dataset contains employee-level information designed to explore factors affecting employee attrition and performance. It is a fictional dataset created by IBM data scientists.

- Number of records: 1,470 employees

- Data types: Mix of numerical (discrete/continuous) and categorical variables

- Objective: Understand employee behavior and identify factors that contribute to attrition.

- The dataset have 35 columns and they are structured as follows:

| Column                   | Type                  | Description                                         |
| ------------------------ | --------------------- | --------------------------------------------------- |
| Age                      | Numeric               | Employee age in years                               |
| Gender                   | Categorical           | Male/Female                                         |
| MaritalStatus            | Categorical           | Married, Single, Other                              |
| Education                | Categorical (1–5)     | 1=Below College, 5=Doctor                           |
| EducationField           | Categorical           | Life Sciences, Medical, Marketing, Technical, Other |
| JobRole                  | Categorical           | Sales Executive, Research Scientist, etc.           |
| Department               | Categorical           | Research & Development, Sales, Other                |
| BusinessTravel           | Categorical           | Travel_Rarely, Travel_Frequently, Other             |
| JobLevel                 | Categorical (1–5)     | Hierarchy level                                     |
| JobSatisfaction          | Categorical (1–4)     | 1=Low, 4=Very High                                  |
| JobInvolvement           | Categorical (1–4)     | 1=Low, 4=Very High                                  |
| WorkLifeBalance          | Categorical (1–4)     | 1=Bad, 4=Best                                       |
| YearsAtCompany           | Numeric               | Total years at company                              |
| YearsInCurrentRole       | Numeric               | Years in current role                               |
| YearsWithCurrManager     | Numeric               | Years with current manager                          |
| YearsSinceLastPromotion  | Numeric               | Years since last promotion                          |
| TrainingTimesLastYear    | Numeric               | Number of trainings last year                       |
| OverTime                 | Categorical (Boolean) | Yes/No                                              |
| PerformanceRating        | Categorical (1–4)     | 1=Low, 4=Outstanding                                |
| EnvironmentSatisfaction  | Categorical (1–4)     | 1=Low, 4=Very High                                  |
| RelationshipSatisfaction | Categorical (1–4)     | 1=Low, 4=Very High                                  |
| MonthlyIncome            | Numeric               | Employee monthly salary                             |
| DailyRate                | Numeric               | Daily pay rate                                      |
| HourlyRate               | Numeric               | Hourly pay rate                                     |
| MonthlyRate              | Numeric               | Monthly pay rate                                    |
| PercentSalaryHike        | Numeric               | % increase in last appraisal                        |
| StockOptionLevel         | Categorical (0–3)     | Number of stock options granted                     |
| DistanceFromHome         | Numeric               | Distance from home to workplace (km)                |
| StandardHours            | Numeric               | Standard work hours (all 80)                        |
| NumCompaniesWorked       | Numeric               | Number of previous employers                        |
| EmployeeCount            | Numeric               | Redundant, all 1                                    |
| EmployeeNumber           | Numeric               | Unique employee ID                                  |
| Attrition                | Categorical (Boolean) | Yes=Employee left, No=Employee stayed               |

## 4. <a name='BusinessRequirements'></a>Business Requirements

The primary business goal of this project is to help the HR department identify and understand the key factors that contribute to employee attrition (resignations).
By analysing patterns in employee data, the project provides actionable insights that can guide strategic HR interventions, improve retention rates, and reduce the cost of turnover.

**Business Objectives:**

1. Predict Attrition Risk:

   - Develop insights and models to identify employees most likely to leave the organisation.

2. Diagnose Causes of Attrition:

   - Determine which factors, such as work-life balance, overtime, compensation, or career progression — most influence employee turnover.

3. Improve Employee Retention:

   - Provide HR managers with data-backed recommendations to reduce attrition and improve engagement.

4. Support Decision-Making with Data Visualization:

   - Create clear, interactive dashboards (in Power BI or Python visualizations) that communicate trends to both technical and non-technical stakeholders.

## 6. <a name='ProjectPlan'></a>Project Plan

| **Phase**                                   | **Tasks**                                                                                                                                                                                          | **Methods / Tools**                                                    | **Expected Outcome**                                                                    |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **1. Data Collection & Understanding**      | - Explore IBM HR dataset<br>- Understand variables, data types, and missing values                                                                                                                 | Python (Pandas, NumPy), Jupyter Notebook                               | Clear understanding of data structure, variable types, and potential issues             |
| **2. Data Cleaning & Preparation**          | - Handle missing/null values<br>- Encode categorical variables (binary/ordinal)<br>                                                                                                                | Python (Pandas, NumPy), Z-score for outlier detection                  | Clean, consistent, and ready-to-analyze dataset                                         |
| **3. Exploratory Data Analysis (EDA)**      | - Descriptive statistics<br>- Correlation analysis<br>- Distribution visualizations (histograms, box plots, bar charts)<br>- Cross-tabulations                                                     | Seaborn, Matplotlib, Plotly, Pandas                                    | Understand patterns, relationships, and anomalies in the data                           |
| **4. Hypothesis Testing & Validation**      | - Work-Life Balance vs Attrition<br>- Overtime vs Attrition<br>- Job Satisfaction vs Attrition<br>- Distance from Home vs Attrition<br>- Career Growth vs Retention<br>- Compensation vs Attrition | Chi-square tests, t-tests, logistic regression, two-proportion z-tests | Statistically validated insights to support or reject hypotheses                        |
| **5. Data Visualization & Reporting**       | - Create bar plots, scatter plots, box plots, and dashboards<br>- Highlight key metrics and trends                                                                                                 | Seaborn, Matplotlib, Plotly, Power BI                                  | Interactive and clear visualizations for HR decision-making                             |
| **6. Predictive Modeling (Optional)**       | - Logistic regression to predict attrition<br>- Evaluate model performance (accuracy, ROC-AUC, confusion matrix)                                                                                   | Python (statsmodels, scikit-learn)                                     | Identify key predictors of attrition and quantify risk probabilities                    |
| **7. Insight Generation & Recommendations** | - Translate analysis into actionable HR strategies<br>- Highlight retention interventions (career growth, work-life balance, compensation, commute, overtime)                                      | Summary reports, Power BI dashboards, documentation                    | Evidence-based recommendations for reducing attrition and improving employee engagement |
| **8. Documentation & Sharing**              | - Prepare README, project report, and visual dashboards<br>- Include methodology, results, and actionable insights                                                                                 | Markdown, Power BI, GitHub, Jupyter Notebook                           | Clear, comprehensive, and reproducible project documentation                            |

## 7. <a name='TheRationaletoMaptheBusinessRequirementstotheDataVisualizations'></a>The Rationale to Map the Business Requirements to the Data Visualizations

Mapping business requirements to data visualizations ensures that each chart, plot, or dashboard is aligned with HR objectives and delivers actionable insights. This approach helps both technical and non-technical stakeholders interpret data efficiently and supports evidence-based decision-making.

| **Business Requirement**                    | **Mapped Visualization**                                                                     | **Rationale / Insight**                                                                                   |
| ------------------------------------------- | -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Identify employees at risk of attrition     | Bar plot of `Attrition` by `WorkLifeBalance`, `OverTime`, `JobSatisfaction`                  | Highlights groups with higher turnover risk for targeted retention programs                               |
| Understand effect of commuting distance     | Bar plot of `Attrition` rate by `DistanceFromHome` bands                                     | Shows how long commutes increase attrition likelihood and informs flexible work policies                  |
| Evaluate career growth impact               | Scatter plot & box plots of `YearsSinceLastPromotion` vs `YearsWithCurrManager` by attrition | Visualizes clustering of employees with limited career growth, guiding promotions and mentorship programs |
| Analyze compensation influence              | Histograms and box plots of `MonthlyIncome` by attrition status                              | Identifies pay gaps affecting turnover, supporting competitive salary structures                          |
| Provide interactive insights for management | Power BI dashboards with KPI cards, trend charts, and filters                                | Allows HR to explore patterns dynamically and monitor key metrics continuously                            |

**Key Benefits:**

- Align Analysis with HR Goals: Ensures visuals answer meaningful business questions.

- Simplify Complex Data: Makes patterns and trends accessible for decision-makers.

- Highlight Actionable Insights: Pinpoints high-risk groups and areas for intervention.

- Support Storytelling: Facilitates communication of findings to executives and managers.

- Bridge Technical & Non-Technical Audiences: Combines statistical rigor with intuitive visuals.

## 8. <a name='AnalysisTechniquesUsed'></a>Analysis Techniques Used

This project applied a combination of statistical analysis, data visualization, and AI-assisted techniques to explore employee attrition patterns and validate hypotheses.
Each method was chosen to extract meaningful insights and present results clearly for both technical and non-technical audiences.

| Step                                                  | Description                                                                                                                                                                                                                 | Tools / Techniques                                                                 |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **1. Data Preparation and Cleaning**                  | Ensured dataset consistency and accuracy by removing nulls/duplicates, converting categorical variables, creating calculated columns (e.g., Distance Bands, Attrition Rate %), verifying data types, and handling outliers. | Python (Pandas, NumPy), Jupyter Notebook, z-score outlier detection                |
| **2. Exploratory Data Analysis (EDA)**                | Explored data distribution, patterns, correlations, and anomalies. Applied descriptive statistics, correlation analysis, distribution plots, and cross-tabulations.                                                         | Pandas, Seaborn, Matplotlib, Histograms, Box plots, Bar charts                     |
| **3. Visual Analytics (Power BI Integration)**        | Designed interactive dashboards to translate analytical results into actionable insights. Used clustered column charts, box plots, scatter plots with trend lines, and KPI cards aligned with business requirements.        | Power BI, Scatter plots, Box plots, KPI cards                                      |
| **4. Model Testing (Optional – Predictive Analysis)** | Applied logistic regression to test predictive relationships for Attrition. Evaluated model using Accuracy, ROC-AUC, and Confusion Matrix.                                                                                  | Python (statsmodels, scikit-learn), Logistic Regression, ROC-AUC, Confusion Matrix |
| **5. AI-Assisted Support and Code Optimisation**      | Leveraged AI tools to suggest efficient code, generate explanations, and optimise repetitive tasks.                                                                                                                         | ChatGPT, GitHub Copilot                                                            |
| **6. Limitations and Alternative Approaches**         | Cross-sectional dataset limits causal inference. Suggested improvements include data balancing (SMOTE), and using decision trees or random forests for better interpretability.                                             | SMOTE, Decision Tree, Random Forest                                                |

## 9. <a name='EthicalConsiderations'></a>Ethical Considerations

Ethical, legal, and social responsibility are essential components of any data analytics project — especially when working with employee information.
This section outlines the key ethical principles, privacy measures, and fairness practices applied throughout the project.

1. Data Privacy and Confidentiality

   - The dataset used is a publicly available and anonymised dataset from Kaggle, containing no personally identifiable information (PII).

   - No names, contact details, or sensitive identifiers (e.g., national insurance numbers) were included.

   - All data was handled in accordance with GDPR principles and general data protection ethics.

   - Any analysis or visualisation was focused on aggregated data (e.g., attrition percentages or average metrics) to ensure individual anonymity.

2. Bias and Fairness

   - The dataset may contain sampling bias, as it reflects a specific company’s employee data and may not generalise to all organisations.

   - Efforts were made to reduce analytical bias by:

   - Using consistent statistical methods for both groups (Attrition = Yes/No).

   - Avoiding assumptions based on demographic variables such as gender or age.

   - Reporting correlations and causations separately to avoid misleading interpretations.

   - Future work could involve testing model fairness across different demographic groups to ensure equitable HR practices.

3. Responsible Data Use

   - Analysis results are intended for research and learning purposes only, not for direct employee evaluation or decision-making.

   - Predictive insights should be used to improve working conditions, not to discriminate against individuals at risk of attrition.

   - Recommendations emphasise positive HR interventions — e.g., better work-life balance, fair pay, and career support — rather than punitive actions.

4. Transparency and Explainability

   - All analytical methods and visualisations are documented openly in the Jupyter Notebook and README.

   - Statistical tests, correlation results, and visual trends are clearly explained in context to maintain transparency for both technical and non-technical audiences.

   - AI-generated code (e.g., from Copilot or ChatGPT) was reviewed and validated to ensure accuracy and ethical compliance.

5. Legal and Social Implications

   - The project adheres to the principles of ethical AI and data governance by promoting fairness, transparency, and accountability.

   - Socially, the goal is to help organisations make data-informed HR decisions that enhance employee wellbeing and equity.

   - The analysis supports ethical workforce management, highlighting the value of using analytics for positive organisational change rather than surveillance.

## 11. <a name='Wireframe'></a>Wireframe

## 12. <a name='KanbanBoard'></a>Kanban Board

- The kanban board screenshots can be found [here](Images)

- The project board can viewed [here](https://github.com/users/RanaAlaaTahon/projects/4)

## 15. <a name='BowerBI Deployment'></a>BowerBI Deployment

## 16. <a name='MainDataAnalysisLibraries'></a>Main Data Analysis Libraries

| **Library**                                                           | **Purpose**                                           |
| --------------------------------------------------------------------- | ----------------------------------------------------- |
| **pandas**                                                            | Data manipulation and analysis                        |
| **numpy**                                                             | Numerical computations                                |
| **matplotlib**                                                        | Basic plotting library                                |
| **seaborn**                                                           | Statistical data visualization with clean styles      |
| **plotly.express**                                                    | Interactive visualizations (simple syntax)            |
| **plotly.graph_objects**                                              | Advanced interactive charts                           |
| **plotly.subplots**                                                   | Combining multiple Plotly figures into subplots       |
| **scipy.stats** (chi2_contingency, ttest_ind, mannwhitneyu, f_oneway) | Hypothesis testing and statistical tests              |
| **pingouin**                                                          | User-friendly statistical tests and effect sizes      |
| **statsmodels**                                                       | Logistic regression and advanced statistical modeling |
| **warnings** (filterwarnings)                                         | Suppress non-critical warnings during analysis        |

## 17. <a name='Credits'></a>Credits

- Kaggle Dataset: [IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- Generative AI tools: ChatGPT, GitHub Copilot

## 18. <a name='Contributors'></a>Contributors

- Rana
- Mike
- Ramaz
- Joy
