# **HR Analytics: Predicting Employee Turnover**

**HR Analytics: Predicting Employee Turnover** is Data-driven exploration of the IBM HR Analytics Employee Attrition &amp; Performance dataset by IBM data scientists. This project analyzes key HR factors such as job satisfaction and work-life balance to predict employee attrition and uncover insights to improve retention and performance.

## 1. <a name='TableofContents'></a>Table of Contents

<details>
  <summary>Click here to expand the contents</summary>

1. [Table of Contents](#TableofContents)
2. [Project Outcomes and Key Findings](#ProjectOutcomesandKeyFindings)
3. [Dataset Content](#DatasetContent)
4. [Business Requirements](#BusinessRequirements)
5. [Hypothesis and Validation](#HypothesisandValidation)
6. [Project Plan](#ProjectPlan)
7. [The Rationale to Map the Business Requirements to the Data Visualizations](#TheRationaletoMaptheBusinessRequirementstotheDataVisualizations)
8. [Analysis Techniques Used](#AnalysisTechniquesUsed)
9. [Ethical Considerations](#EthicalConsiderations)
10. [Dashboard Design](#DashboardDesign)
11. [Wireframe](#Wireframe)
12. [Kanban Board](#KanbanBoard)
13. [Unfixed Bugs](#UnfixedBugs)
14. [Development Roadmap](#DevelopmentRoadmap)
15. [PowerBI Deployment](#PowerBIDeployment)
16. [Main Data Analysis Libraries](#MainDataAnalysisLibraries)
17. [Credits](#Credits)
18. [Contributors](#Contributors)
19. [Acknowledgements](#Acknowledgements)

</details>

## 2. <a name='ProjectOutcomesandKeyFindings'></a>Project Outcomes and Key Findings

This project explores key factors influencing employee attrition using the IBM HR Analytics Employee Attrition dataset from Kaggle
.
The goal is to identify which features most strongly predict employee turnover and to develop data-driven recommendations for improving employee retention and satisfaction.

Through exploratory data analysis (EDA), statistical testing, and data visualization, the project validates multiple hypotheses about work-life balance, overtime, job satisfaction, distance from home, career growth, and compensation.

🎯 Objectives

Analyse employee behaviour to identify attrition trends.

Evaluate the impact of work-life balance, compensation, and career development on employee retention.

Build data visualisations and statistical summaries to explain key predictors of attrition.

Support HR decision-making with clear, interpretable insights.

## 3. <a name='DatasetContent'></a>Dataset Content

## 4. <a name='BusinessRequirements'></a>Business Requirements

The primary business goal of this project is to help the HR department identify and understand the key factors that contribute to employee attrition (resignations).
By analysing patterns in employee data, the project provides actionable insights that can guide strategic HR interventions, improve retention rates, and reduce the cost of turnover.

## Business Objectives

### 1. Predict Attrition Risk:
Develop insights and models to identify employees most likely to leave the organisation.

### 2. Diagnose Causes of Attrition:
Determine which factors — such as work-life balance, overtime, compensation, or career progression — most influence employee turnover.

### 3. Improve Employee Retention:
Provide HR managers with data-backed recommendations to reduce attrition and improve engagement.

### 4. Support Decision-Making with Data Visualisation:
Create clear, interactive dashboards (in Power BI or Python visualisations) that communicate trends to both technical and non-technical stakeholders.

## 5. <a name='HypothesisandValidation'></a>Hypothesis and Validation

## 6. <a name='ProjectPlan'></a>Project Plan

## 7. <a name='TheRationaletoMaptheBusinessRequirementstotheDataVisualizations'></a>The Rationale to Map the Business Requirements to the Data Visualizations

Each business requirement is linked to targeted data visualisations that provide actionable, evidence-based insights.
This section explains why each visualisation was chosen and how it supports HR decision-making.

Business Requirement	Data Visualisation Used	Rationale / Purpose
Identify overall attrition patterns across departments	Donut / Pie Chart – Attrition Distribution %	Gives a quick, high-level overview of how many employees have left vs. stayed. Helps management monitor the overall turnover rate.
Analyse the effect of Work-Life Balance on attrition	Bar Chart – Average Attrition % by Work-Life Balance	Visually compares attrition across balance ratings (Good, Fair, Poor). Clarifies whether lower balance is a major risk factor.
Examine Overtime and Attrition	Clustered Column Chart – Attrition Rate by Overtime Status	Demonstrates that employees who frequently work overtime show significantly higher attrition levels.
Assess impact of Job Satisfaction on attrition	Box Plot – Job Satisfaction vs. Attrition	Displays the distribution of satisfaction scores across both attrition groups, showing how dissatisfaction correlates with turnover.
Measure Distance from Home effects	Bar Chart – Attrition Rate by Distance Band (0–5 km, 6–10 km, etc.)	Highlights whether long commutes increase the likelihood of resignation.
Evaluate Career Growth and Retention	Scatter Plot / Regression Line – Years Since Promotion vs. Years With Manager	Shows relationship between promotion opportunities, manager tenure, and attrition. Visual trendlines reveal stagnation effects.
Compare Compensation levels	Histogram / Bar Chart – Attrition % by Income Range	Highlights how lower monthly income correlates with higher turnover, supporting fair pay policy recommendations.
Explore Correlations among all variables	Heatmap – Correlation Matrix	Helps analysts see relationships between multiple features like salary, promotion, and job satisfaction at once.
Provide a full HR overview	Power BI Dashboard Page with KPIs: Avg Age, Avg Salary, Attrition %, Overtime %, Satisfaction Score	A dynamic summary page allows HR and management to monitor live metrics and compare across roles or departments.
🧭 Example Dashboard Structure
Page Name	Content / Visuals Included	Purpose
Overview Page	KPI cards, Attrition Donut Chart, Department Breakdown	High-level overview of employee retention status.
Work-Life & Overtime Page	Clustered Bar Charts, Filters	Validate impact of work-life balance and overtime hours.
Satisfaction & Career Growth Page	Box Plots, Scatter Charts, Regression Trend	Explore job satisfaction, promotion, and manager tenure relationships.
Compensation Analysis Page	Bar and Line Charts	Identify salary-related attrition risks.
Predictive Insights Page	Decomposition Tree or Decision Tree Visual	Allow HR to drill down by department, gender, and experience level.
## 8. <a name='AnalysisTechniquesUsed'></a>Analysis Techniques Used

This project applied a combination of statistical analysis, data visualisation, and AI-assisted techniques to explore employee attrition patterns and validate hypotheses.
Each method was chosen to extract meaningful insights and present results clearly for both technical and non-technical audiences.

-  1. Data Preparation and Cleaning

Before analysis, the dataset was cleaned using Python (Pandas) to ensure consistency and accuracy:

Removed null or duplicate records.

Converted categorical variables (e.g., Attrition, Overtime) to binary or ordinal format.

Created calculated columns such as Distance Bands and Attrition Rate % for better grouping.

Verified data types and handled outliers using z-score methods.

Tools: Pandas, NumPy, Jupyter Notebook

-  2. Exploratory Data Analysis (EDA)

EDA was used to understand data distribution, patterns, and potential anomalies.
Visualisations were produced using Seaborn, Matplotlib, and later adapted into Power BI dashboards.

Techniques applied:

Descriptive statistics: mean, median, standard deviation for numeric variables.

Correlation analysis: identified relationships between features such as distance, income, and satisfaction.

Distribution plots: histograms, box plots, and bar charts for comparing groups (Attrition = Yes/No).

Cross-tabulations: between categorical variables like JobRole, OverTime, and WorkLifeBalance.

-  3. Visual Analytics (Power BI Integration)

Power BI was used to design interactive dashboards that translate analytical results into actionable visuals:

Clustered column charts to show trends (e.g., overtime vs attrition).

Box plots to display distribution differences between groups.

Scatter plots with trend lines to visualise correlations.

KPI cards to highlight summary metrics such as total attrition rate, average salary, and satisfaction score.

Each visualisation was mapped to a business requirement, ensuring alignment between analytical evidence and organisational goals.

-  4. Model Testing (Optional – Predictive Analysis)

A simple logistic regression model was applied to test predictive relationships:

Target variable: Attrition (Yes/No)

Predictors: WorkLifeBalance, OverTime, JobSatisfaction, DistanceFromHome, YearsSinceLastPromotion, MonthlyIncome

Model evaluation metrics: Accuracy, ROC-AUC, and Confusion Matrix.

This model supported validation of which features were the most statistically significant in predicting turnover.

-  5. AI-Assisted Support and Code Optimisation

Generative AI tools (like GitHub Copilot and ChatGPT) were used to:

Suggest efficient code for data cleaning and visualisation.

Generate explanations and insights for storytelling sections.

Optimise repetitive analysis tasks and documentation templates.

-  6. Limitations and Alternative Approaches

The dataset is cross-sectional, so it measures correlation, not causation.

Balancing data using SMOTE or stratified sampling could improve model accuracy.

A decision tree or random forest model could provide stronger prediction interpretability.

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

## 10. <a name='DashboardDesign'></a>Dashboard Design

## 11. <a name='Wireframe'></a>Wireframe

## 12. <a name='KanbanBoard'></a>Kanban Board

## 13. <a name='UnfixedBugs'></a>Unfixed Bugs

## 14. <a name='DevelopmentRoadmap'></a>Development Roadmap

### Future Considerations

- Integration with employee wellness programs
- Diversity and inclusion analytics
- Skills gap analysis and training recommendations
- Succession planning insights
- Cost-benefit analysis for retention initiatives

## 15. <a name='PowerBIDeployment'></a>PowerBI Deployment

### PowerBI Deployment
This project includes PowerBI reports and dashboards that visualise key data insights.

### Important Licensing Note:
Due to our license restrictions, the license we currently have does not allow the report to be published to the PowerBI Service for sharing.

### Deployment Details:
- The PowerBI (.pbix) file can be found here in the repository for local use.

- Normally, deployment involves:

  1. Developing reports locally in PowerBI Desktop.

  2. Publishing reports to the PowerBI Service workspace for access and collaboration.

  3. Configuring data sources, gateways, and scheduled refresh.

  4. Managing permissions and sharing dashboards with stakeholders.

  5. Optionally embedding reports in applications or websites.

Because our license restricts publishing, users will need to open the .pbix file locally or upgrade licenses to enable cloud sharing.

## 16. <a name='MainDataAnalysisLibraries'></a>Main Data Analysis Libraries

| Library      | Example Use                                 |
| ------------ | ------------------------------------------- |
| pandas       | Data cleaning, merging, feature engineering |
| numpy        | Numeric computation, anomaly calculations   |
| matplotlib   | Time Series, bar chart                      |
| seaborn      | Histogram, Correlation, Box Plot, Violin    |
| plotly       | Interactive mapping and dashboards          |
| scikit-learn | Machine Learning in Python                  |

## 17. <a name='Credits'></a>Credits

**Data Sources:** [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/)

**AI assistance** for brainstorming, code structuring, and documentation

## 18. <a name='Contributors'></a>Contributors

Rana 
Mike 
Ramaz 
Joy 

## 19. <a name='Acknowledgements'></a>Acknowledgements

* A big thank you to:
  - Vasi Pavaloi, a facilitator for this course, for all his support and helpful advice throughout the project.
  - Niel McEwen, a subject expert at Code Institue