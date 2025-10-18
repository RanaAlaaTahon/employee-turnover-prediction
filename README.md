# **HR Analytics: Predicting Employee Turnover**

**HR Analytics: Predicting Employee Turnover** is a Data-driven exploration of the IBM HR Analytics Employee Attrition &amp; Performance dataset by IBM data scientists. This project analyzes key HR factors such as job satisfaction and work-life balance to predict employee attrition and uncover insights to improve retention and performance.

## 1. <a name='TableofContents'></a>Table of Contents

<details>
  <summary>Click here to expand the contents</summary>

1. [Table of Contents](#TableofContents)
2. [Project Outcomes and Key Findings](#ProjectOutcomesandKeyFindings)
3. [Dataset Content](#DatasetContent)
4. [Business Requirements](#BusinessRequirements)
5. [Hypothesis and Validation](#HypothesisandValidation)
6. [Project Plan](#ProjectPlan)
7. [The Rationale to Map the Business Requirements to the Data Visualisations](#TheRationaletoMaptheBusinessRequirementstotheDataVisualizations)
8. [Analysis Techniques Used](#AnalysisTechniquesUsed)
9. [Ethical Considerations](#EthicalConsiderations)
10. [Dashboard Design](#DashboardDesign)
11. [Wireframe](#Wireframe)
12. [Kanban Board](#KanbanBoard)
13. [Unfixed Bugs](#UnfixedBugs)
14. [Development Roadmap](#DevelopmentRoadmap)
15. [Tableau Deployment](#TableauDeployment)
16. [Main Data Analysis Libraries](#MainDataAnalysisLibraries)
17. [Credits](#Credits)
18. [Contributors](#Contributors)
19. [Acknowledgements](#Acknowledgements)

</details>

## 2. <a name='ProjectOutcomesandKeyFindings'></a>Project Outcomes and Key Findings

| Hypothesis                              | Outcome / Validation                                       | Key Findings                                                                                                                                                                                                                                                                   | Implications for HR                                                                                                                                    |
| --------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1. Work-Life Balance and Attrition**  | Chi-square test, bar plot, logistic regression             | - Poor work-life balance is associated with higher attrition (level 1: 31.3%). <br> - Statistically significant relationship confirmed (χ² = 16.325, p = 0.001). <br> - Logistic regression shows β = -0.24, p = 0.014.                                                        | - Introduce flexible hours and mental health/recharge days. <br> - Conduct regular employee surveys to monitor work-life balance.                      |
| **2. Overtime and Employee Attrition**  | Chi-square test, logistic regression, bar plots            | - Employees working overtime have significantly higher attrition (~30% vs 10%). <br> - Strong statistical correlation (chi² = 89, p < 0.05).                                                                                                                                   | - Monitor overtime hours to prevent burnout. <br> - Consider workload redistribution or compensation incentives.                                       |
| **3. Job Satisfaction and Attrition**   | Independent-samples t-test, Mann-Whitney U test, box plots | - Lower job satisfaction is strongly associated with higher attrition. <br> - Statistical tests confirm significant difference (p < 0.05). <br> - Attrition decreases as job satisfaction increases.                                                                           | - Implement employee engagement programs to improve satisfaction. <br> - Address dissatisfaction drivers through feedback and recognition systems.     |
| **4. Distance from Home and Attrition** | Binned distance analysis, bar plots, logistic regression   | - Attrition increases with greater commuting distance. <br> - Employees living 20–30 km away have the highest attrition (~22%). <br> - Logistic regression confirms commuting distance as a significant factor.                                                                | - Offer flexible or remote work options. <br> - Consider transportation support or relocation assistance for distant employees.                        |
| **5. Career Growth and Retention**      | Scatter plots, box plots, correlation analysis             | - Employees with fewer promotions or shorter tenure with current manager have higher attrition. <br> - Moderate correlation between promotion history and manager tenure (r = 0.51). <br> - Employees who stayed had longer tenure with managers and slightly more promotions. | - Provide structured promotion pathways and career development plans. <br> - Foster stable manager-employee relationships through mentorship programs. |
| **6. Compensation and Attrition**       | Independent-samples t-test, histograms, box plots          | - Employees who left had significantly lower monthly income than those who stayed. <br> - Large mean difference ($2,045.65) between groups. <br> - Statistical tests strongly reject null hypothesis (t-statistic = -6.2039, p < 0.000001).                                    | - Review and adjust compensation structures for lower-income employees. <br> - Ensure pay equity and performance-based incentives to retain talent.    |

**Overall Project Outcomes:**

- Attrition Drivers Identified: Work-life balance, overtime, job satisfaction, distance from home, career growth, and compensation were all statistically validated as significant predictors of employee attrition.

- Visual and Statistical Confirmation: Multiple visualisation techniques (bar plots, scatter plots, box plots, histograms) were combined with statistical tests (t-test, chi-square, Mann-Whitney U, logistic regression) to ensure robust validation.

- Actionable Insights for HR:

  - Flexible work arrangements and workload management.

  - Employee engagement and satisfaction programs.

  - Structured promotion pathways and mentorship programs.

  - Competitive compensation, especially for lower-income brackets.

- Predictive Analysis Foundation: Logistic regression models demonstrated which factors most strongly influence turnover, providing a foundation for predictive HR analytics.

## 3. <a name='DatasetContent'></a>Dataset Content

The IBM HR Analytics dataset contains employee-level information designed to explore factors affecting employee attrition and performance. It is a fictional dataset created by IBM data scientists.

- Number of records: 1,470 employees

- Data types: Mix of numerical (discrete/continuous) and categorical variables

- Objective: Understand employee behavior and identify factors that contribute to attrition.

- The dataset has 35 columns and they are structured as follows:

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

## 5. <a name='HypothesisandValidation'></a>Hypothesis and Validation

| #                                       | Hypothesis                                                                                     | Validation Method                                                                                                                                                                                                                                                        | Null Hypothesis (H₀)                                                                                               | Alternative Hypothesis (H₁)                                                                                             |
| --------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **1. Work-Life Balance and Attrition**  | Employees with poor work-life balance are more likely to leave the company.                    | - Encode `Attrition` as binary (1=Yes, 0=No)<br>- Compare attrition rates across `WorkLifeBalance` categories<br>- Bar plot of attrition rate by `WorkLifeBalance`<br>- Chi-square test of independence<br>- Logistic regression (`Attrition_encoded ~ WorkLifeBalance`) | There is no significant relationship between `WorkLifeBalance` and attrition.                                      | There is a significant relationship between `WorkLifeBalance` and attrition.                                            |
| **2. Overtime and Employee Attrition**  | Employees who work overtime are significantly more likely to quit.                             | - Two-proportion z-test or chi-square test comparing `OverTime` (Yes/No) vs `Attrition`<br>- Plot attrition rates by `OverTime` status<br>- Logistic regression with `OverTime` as predictor                                                                             | There is no significant correlation between `OverTime` and `Attrition`.                                            | Employees who work overtime have a significantly higher likelihood of leaving.                                          |
| **3. Job Satisfaction and Attrition**   | Lower job satisfaction leads to higher attrition.                                              | - Independent-samples t-test comparing `JobSatisfaction` for `Attrition = Yes` vs `No`<br>- Box/violin plots of `JobSatisfaction` by `Attrition`<br>- (Optional) Logistic regression including `JobSatisfaction`                                                         | There is no significant difference in `JobSatisfaction` between employees who left and those who stayed.           | Employees with lower `JobSatisfaction` are more likely to leave.                                                        |
| **4. Distance from Home and Attrition** | Employees who live farther from work are more likely to leave the company.                     | - Create distance bins (0–5 km, 6–10 km, 11–20 km, 20–30 km)<br>- Calculate attrition rate per distance band<br>- Bar plot of attrition rate by distance band                                                                                                            | There is no significant relationship between `DistanceFromHome` and attrition.                                     | Employees living farther from work have a significantly higher likelihood of attrition.                                 |
| **5. Career Growth and Retention**      | Employees with fewer promotions or shorter tenure with their manager are more likely to leave. | - Scatter plot: `YearsSinceLastPromotion` vs `YearsWithCurrManager` colored by attrition<br>- Add regression trend line for `Attrition=Yes`<br>- Box plots comparing `YearsSinceLastPromotion` and `YearsWithCurrManager` between groups                                 | Career growth metrics (`YearsSinceLastPromotion`, `YearsWithCurrManager`) have no significant effect on attrition. | Limited career growth (fewer promotions or shorter tenure with current manager) significantly increases attrition risk. |
| **6. Compensation and Attrition**       | Employees with lower monthly income are more likely to leave.                                  | - Separate `MonthlyIncome` by attrition status<br>- Independent-samples t-test to compare mean income<br>- Visualize income distributions with histograms and box plots                                                                                                  | There is no significant difference in `MonthlyIncome` between employees who left and those who stayed.             | Employees who left have significantly lower `MonthlyIncome` than those who stayed.      


## 🧩 Employee Attrition – Machine Learning Summary

### Overview

This project investigates the key factors influencing employee attrition using the IBM HR Analytics dataset.  
Machine learning models were developed to predict which employees are most at risk of leaving and to identify the strongest drivers of turnover.

### Machine Learning Process

1. **Data Preparation** – Cleaned and encoded categorical variables (e.g. `OverTime`, `Attrition`, `JobRole`),  
   treating ordinal and continuous features appropriately.
2. **Exploratory Analysis** – Examined attrition by satisfaction, tenure, overtime and income levels.
3. **Model Development** – Trained multiple tree-based models (**Decision Tree**, **Random Forest**, **Extra Trees**, **XGBoost**)  
   and optimised them using **GridSearchCV** with AUC, F1 and Recall scoring.
4. **Model Evaluation** – Compared performance using ROC-AUC, recall, F1 and balanced accuracy.  
   **Random Forest** and **XGBoost** emerged as the best-performing and most stable models.
5. **Interpretation** – Analysed feature importance and visualised results through precision–recall curves and confusion matrices.

### Key Findings vs Hypotheses

| Hypothesis | Outcome |
|-------------|----------|
| **1. Work–Life Balance** | Poor work–life balance is associated with higher attrition. |
| **2. Overtime** | Employees working overtime are significantly more likely to leave. |
| **3. Job Satisfaction** | Lower job satisfaction strongly correlates with higher attrition. |
| **4. Distance from Home** | Attrition increases with greater commuting distance. |
| **5. Career Growth** | Fewer promotions or shorter tenure with a manager increase attrition. |
| **6. Compensation** | Employees who left earned noticeably lower monthly income than those who stayed. |

### Conclusions

- **XGBoost** and **Random Forest** achieved the best balance between accuracy and recall.  
- **Recall-focused tuning** improved the ability to identify leavers without major loss of precision.  
- Findings support all six hypotheses, confirming that attrition is influenced by workload, satisfaction, tenure and pay equity.  
- Insights can guide HR teams to improve retention by promoting better work–life balance, fair compensation and career progression.

#### Next Steps

- Train models with more extensive parameter grids.
- Optimise the training process by creating reusable functions.
- Run models with Clustering & Regression algorithms.

---

                                |

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

   - The dataset used is a publicly available from Kaggle, containing no personally identifiable information (PII).

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

## 10. <a name='DashboardDesign'></a>Dashboard Design

The Employee Attrition & Retention Dashboard was developed in Power BI to visualize key employee trends, test hypotheses, and provide actionable insights for HR decision-making.
It aligns directly with the statistical and visual analyses performed in Python and highlights business-relevant metrics such as attrition rate, compensation, and career growth.

![Dashboard](/Images/dashboard.png)

| KPI                                  | Description                                                           |
| ------------------------------------ | --------------------------------------------------------------------- |
| **Total Employees (1,470)**          | Displays the total workforce size.                                    |
| **Attrition Count (237)**            | Number of employees who have left the organization.                   |
| **Attrition Rate (0.16 or 16%)**     | Percentage of total employees who have left.                          |
| **Average Work-Life Balance (2.76)** | Mean rating (scale 1–4) reflecting employee work-life balance.        |
| **Average Job Satisfaction (2.73)**  | Mean satisfaction rating (scale 1–4) showing general job contentment. |

| Visualization                                                               | Purpose                                                            | Key Insights                                                                      |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| **Attrition Rate by Years Since Last Promotion (Line Chart)**               | Examine how promotion timing affects attrition.                    | Attrition increases for employees with either very recent or very old promotions. |
| **Attrition Rate by Distance from Home (Bar Chart)**                        | Show the relationship between commute distance and turnover.       | Employees living 20–30 km away show the highest attrition (~22%).                 |
| **Sum of Monthly Income by JobRole and Attrition (Clustered Column Chart)** | Compare salary distributions across roles for leavers vs. stayers. | Higher-income roles (e.g., Managers, Sales Executives) show lower attrition.      |
| **Filters: JobRole, OverTime**                                              | Enable interactive exploration by department or overtime status.   | Dynamic insights allow customized HR analysis by specific employee segments.      |

## 11. <a name='Wireframe'></a>Wireframe

The wireframe designed using Figma to serve as a blueprint for dashboard layout and navigation, ensuring intuitive flow, visual balance, and consistent user experience before actual Power BI implementation.

![Wireframe](/Images/wireframe.png)

## 12. <a name='KanbanBoard'></a>Kanban Board

- The kanban board screenshots can be found [here](Images)

- The project board can viewed [here](https://github.com/users/RanaAlaaTahon/projects/4)

## 13. <a name='UnfixedBugs'></a>Unfixed Bugs

- There are currently no known bugs or unresolved issues in this project.

- All analyses, visualizations, and scripts have been tested and validated to work as expected.

- If any issues are discovered in the future, they will be documented here and addressed promptly.

## 14. <a name='DevelopmentRoadmap'></a>Development Roadmap

| **Phase**                                 | **Description**                            | **Planned Enhancements / Actions**                                                                                                       |
| ----------------------------------------- | ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Data Enhancement**                   | Improve dataset quality and coverage       | Integrate additional datasets (e.g., engagement surveys, exit interviews), implement automated data cleaning pipelines                   |
| **2. Advanced Analytics & Modeling**      | Strengthen predictive capabilities         | Apply Random Forest, Gradient Boosting, XGBoost; evaluate feature importance; implement survival analysis or time-series modeling        |
| **3. Interactive Dashboards & Reporting** | Enhance visualization and usability        | Expand Power BI dashboards with drill-downs and filters; add predictive alerts for HR; scenario analysis by department, tenure, and role |
| **4. Automation & AI Integration**        | Increase efficiency and insights           | Automate report generation; integrate AI-assisted insights for trend detection; allow natural language querying of HR metrics            |
| **5. Optimization & Scalability**         | Prepare for production and large-scale use | Optimize code performance; containerize project with Docker; deploy on cloud platforms (Azure/AWS)                                       |
| **6. HR Policy Simulation**               | Test HR strategies                         | Develop “what-if” simulations (flexible hours, salary adjustments, promotion cycles) to forecast impact on attrition                     |
| **7. Documentation & Collaboration**      | Improve reproducibility and usability      | Maintain comprehensive analysis documentation; establish Git/GitHub version control; create user guides for stakeholders                 |

## 15. <a name='Bower BI Deployment'></a>BowerBI Deployment

This project includes Power BI reports and dashboards that visualise key data insights.

**Important Licensing Note:**
Due to our license restrictions, the license we currently have does not allow the report to be published to the Power BI Service for sharing.

**Deployment Details:**

- The Power BI (.pbix) file can be found here in the repository for local use.

- Normally, deployment involves:

  1. Developing reports locally in PowerBI Desktop.

  2. Publishing reports to the PowerBI Service workspace for access and collaboration.

  3. Configuring data sources, gateways, and scheduled refresh.

  4. Managing permissions and sharing dashboards with stakeholders.

  5. Optionally embedding reports in applications or websites.

- Because our license restricts publishing, users will need to open the .pbix file locally or upgrade licenses to enable cloud sharing.

## 16. <a name='MainDataAnalysisLibraries'></a>Main Data Analysis Libraries

| **Library**                                                           | **Purpose**                                           |
| --------------------------------------------------------------------- | ----------------------------------------------------- |
| **pandas**                                                            | Data manipulation and analysis                        |
| **numpy**                                                             | Numerical computations                                |
| **matplotlib**                                                        | Basic plotting library                                |
| **seaborn**                                                           | Statistical data visualisation with clean styles      |
| **plotly.express**                                                    | Interactive visualisations (simple syntax)            |
| **plotly.graph_objects**                                              | Advanced interactive charts                           |
| **plotly.subplots**                                                   | Combining multiple Plotly figures into subplots       |
| **scipy.stats** (chi2_contingency, ttest_ind, mannwhitneyu, f_oneway) | Hypothesis testing and statistical tests              |
| **pingouin**                                                          | User-friendly statistical tests and effect sizes      |
| **statsmodels**                                                       | Logistic regression and advanced statistical modeling |
| **warnings** (filterwarnings)                                         | Suppress non-critical warnings during analysis        |

## 17. <a name='Credits'></a>Credits

**Data Sources:** [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/)

**AI assistance tools:** ChatGPT, Copilot for brainstorming, code structuring and documentation.

## 18. <a name='Contributors'></a>Contributors

- Rana
- Mike
- Ramaz
- Joy

## 19. <a name='Acknowledgements'></a>Acknowledgements

**A big thank you to:**

- Vasi Pavaloi, a facilitator for this course, for all his support and helpful advice throughout the project.
- Niel McEwen, a subject expert at Code Institue
