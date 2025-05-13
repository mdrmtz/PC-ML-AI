# Predicting Core Web Vitals Performance based on Website Characteristics

**Miguel Daniel Ramos Martinez**

#### Executive summary
This research project aims to develop predictive models for Core Web Vitals (LCP, INP, and CLS) by analyzing various website characteristics. By leveraging machine learning techniques and data from the Chrome User Experience Report, HTTP Archive, and Blue Triangle RUM, the study will identify key factors influencing website performance. The outcome will be actionable insights and tools that empower developers and website owners to optimize their sites for improved user experience and search engine rankings.

#### Rationale
Core Web Vitals are crucial metrics for evaluating website user experience, directly impacting search engine rankings and user satisfaction. Understanding the relationship between website attributes and these metrics allows for proactive optimization, leading to:

* Improved search engine visibility
* Enhanced user engagement and conversion rates
* Better overall website performance
* More efficient resource allocation for development teams
* Data-driven decision-making for technology choices

#### Research Question

Which measurable website attributes (derived from CrUX, HTTP Archive, and Blue Triangle RUM data) are the most significant predictors of Core Web Vitals (LCP, INP, and CLS) performance?

#### Data Sources
1. Real User Monitoring (RUM) Data (Blue Triangle): Performance data specific to our client's website, potentially offering more granular insights and custom metrics beyond standard CrUX data. This can complement the CrUX data and provide a deeper understanding of our specific context.

#### Methodology

The [Capstone(EDA)](Capstone(EDA).ipynb) notebook implements the CRISP-DM framework, including:

1. **Data Acquisition and Preparation:** Collection, cleaning, integration, and preprocessing of data from Blue Triangle RUM. The notebook demonstrates handling of missing values and data consistency.
2. **Feature Engineering:** Derivation of new features (e.g., Performance Score,fcp_category interaction_lcp_tbt) from the raw data, as detailed in the notebook.
3. **Exploratory Data Analysis (EDA):** The notebook contains visualizations (histograms, scatter plots, box plots, etc.) to understand data distributions, identify relationships, and detect potential issues like outliers.
4. **Baseline Machine Learning Model**: A classification model will be implemented to predict performance score based on the derived input features.
5. **Regression Analysis:** Random Forest Regression to predict Performance Score(based on Core Web Vitals). The notebook shows the model building and evaluation process.
6. **Model Evaluation:** The notebook calculates Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared to assess model performance. **A clear rationale for the selection and use of these evaluation metrics is provided within the notebook.** The interpretation of these metrics in the context of the prediction task is also detailed there.
7. **Analysis and Interpretation:** Identification of significant predictors and interpretation of model results, presented clearly in the notebook. Clustering analysis (if performed) will also be detailed there.

#### Results
* (The findings of the research, including the **valid interpretation of the evaluation metrics**, will be detailed in the [Capstone(EDA)](Capstone(EDA).ipynb) notebook.)
* Key website attributes impacting LCP, INP, and CLS will be identified in the notebook.
* Quantification of relationships between attributes and Core Web Vitals will be presented in the notebook.
* Model predictive accuracy will be evaluated and shown in the notebook.
* Insights into website performance patterns and optimization areas will be discussed in the notebook.

#### Next steps
* Refine the predictive models based on the initial results.
* Explore additional machine learning techniques.
* Investigate the impact of specific website technologies in more detail.
* Develop a tool or dashboard to visualize the relationships between website attributes and Core Web Vitals.
* Validate the findings with a larger and more diverse dataset.
* Apply the models to predict Core Web Vitals for a wider range of websites.
* Develop recommendations and best practices for website optimization based on the research findings.

#### Outline of project

- [Capstone Assignment 20.1: Initial Report and Exploratory Data Analysis (EDA)](Capstone(EDA).ipynb)


##### Contact and Further Information
[Linkedin](https://www.linkedin.com/in/mdrmtz/)
Founder | Technical Leader | AI/ML | Product Owner | Web Performance | Google Cloud | Agile | Consulting Services | International Speaker
