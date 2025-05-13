# Module 6 Capstone Assignment 6.1: Draft the Problem Statement

## Problem Statement
A prediction model for Core Web Vitals performance based on website characteristics.

## General Overview
This project aims to develop predictive models for Core Web Vitals—**Largest Contentful Paint (LCP)**, **Interaction to Next Paint (INP)**, and **Cumulative Layout Shift (CLS)**—using machine learning. The objective is to quantify the relationship between measurable website attributes and real-user performance, enabling proactive performance optimization.

## Data Requirements

1. **Core Web Vitals (CrUX - Chrome User Experience Report)**
    - Source of target variables (LCP, INP, CLS).
    - Accessible via CrUX API or BigQuery.

2. **Website Structure and Resource Data (HTTP Archive - har.org)**
    - Includes metrics related to page structure and resource loading:
        - DOM depth, number of DOM elements.
        - Number and size of images, scripts, CSS, and other resources.
        - Resource loading order and timing.
        - HTTP response headers (e.g., caching directives, content encoding).

3. **Technology Stack and Infrastructure (e.g., BuiltWith, manual inspection, web scraping)**
    - Identifies use of:
        - Frameworks (e.g., React, Angular, Vue.js).
        - CMS platforms (e.g., Adobe Experience Manager, WordPress).
        - CDNs.

## Potential Techniques

### Predictive Modeling

- **Linear Regression**  
  Baseline model for continuous Core Web Vitals metrics.

- **Random Forests**  
  Captures non-linear relationships and enables feature importance analysis.

- **Support Vector Regression (SVR)**  
  Effective in high-dimensional spaces, supporting complex, non-linear patterns.

### Feature Engineering & Dimensionality Reduction

- **Feature Engineering**  
  Derives metrics like total image size, text-to-image ratio, number of blocking scripts, and JavaScript execution time.

- **Principal Component Analysis (PCA)**  
  Reduces dimensionality while preserving relevant information to optimize performance and reduce complexity.

### Clustering

- **K-Means Clustering**  
  Groups websites with similar characteristics or performance metrics, enabling targeted regression models.

- **DBSCAN**  
  Identifies clusters of varying shapes and sizes, useful for detecting outliers with anomalous performance.

---

# Module 16 Capstone Assignment 16.1: Finalizing Your Problem Statement

## Research Purpose

To identify which website attributes most significantly impact Core Web Vitals measurements:

- **LCP** (Largest Contentful Paint)
- **INP** (Interaction to Next Paint)
- **CLS** (Cumulative Layout Shift)

## Data Sources

1. **Chrome User Experience Report (CrUX)**
    - Accessed via API or BigQuery.

2. **HTTP Archive (har.org)**
    - Provides structural and resource-loading data.

3. **Blue Triangle RUM**
    - Real User Monitoring data from current client engagements.

## Methodology

### Predictive Modeling

- Linear Regression
- Random Forests
- Support Vector Regression (SVR)
- Additional regression methods as appropriate

### Dimensionality Reduction

- **Principal Component Analysis (PCA)**
    - Applied post-feature engineering.

### Clustering

- **K-Means**
- **DBSCAN**
    - For segmenting data and identifying anomalies.

## Expected Outcome

- Accurate prediction of **Core Web Vitals** from website attributes.
- Identification of key performance-influencing characteristics.
- Establishment of measurable correlations between website features and performance metrics.

## Practical Impact

This research will:

- Enable **developers and website owners** to:
    - Optimize performance proactively.
    - Make strategic technology choices.

- Support **product owners** in:
    - Prioritizing improvements based on real-world data.
    - Targeting performance-sensitive components.

- Help **organizations**:
    - Align performance goals with business timelines.
    - Drive data-informed decisions for development priorities.
    - Shorten the cycle time for performance optimizations.

# Module 20 Capstone Assignment 20.1: Initial Report and Exploratory Data Analysis (EDA)

## Performing exploratory data analysis (EDA) to develop an initial report for your capstone project

- [See README](InitialReportAndExploratoryDataAnalysis(EDA)/README.md)
