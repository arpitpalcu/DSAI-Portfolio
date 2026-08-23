\# Customer Segmentation \& Revenue Intelligence



\## Project Overview



This project uses unsupervised machine learning to identify meaningful customer

segments based on customer value, transaction behavior, recent engagement,

age, and income.



The objective is to transform customer-level data into actionable business

segments that can support customer retention, personalization, cross-selling,

and targeted marketing strategies.



\---



\## Business Problem



Businesses often have a large and diverse customer base with different levels

of activity, purchasing behavior, and customer value.



The key business question addressed in this project is:



> Can customer behavior and profile characteristics be used to identify

> distinct customer segments and develop targeted business strategies?



\---



\## Analytical Approach



The project follows an end-to-end customer segmentation workflow:



1\. Data loading and quality assessment

2\. Data cleaning and privacy-aware feature selection

3\. Exploratory data analysis

4\. Revenue feature engineering

5\. Transaction and engagement feature engineering

6\. Missing-value treatment

7\. Log transformation of skewed numerical features

8\. Feature scaling

9\. K-Means clustering

10\. Silhouette-score evaluation

11\. Customer segment profiling

12\. Business recommendations



\---



\## Features Used for Segmentation



The final segmentation model uses seven business-oriented features:



\- Revenue\_Recent

\- Revenue\_Recent\_Ratio

\- Revenue\_Per\_Transaction\_3M

\- Transactions\_3M\_Avg

\- Transaction\_Recent\_Ratio

\- Age

\- Income



These features represent customer value, recent revenue behavior,

transaction engagement, customer profile, and income.



\---



\## Model Selection



K-Means clustering was evaluated using multiple cluster counts:



\- K = 2

\- K = 3

\- K = 4

\- K = 5

\- K = 6

\- K = 7

\- K = 8



Silhouette analysis identified:



\*\*Optimal K = 3\*\*



with a silhouette score of approximately:



\*\*0.281\*\*



The cluster count was therefore selected based on the evaluated clustering

performance rather than being chosen arbitrarily.



\---



\## Customer Segments



\### 1. High-Engagement Core Customers



\- Customers: 31,612

\- Customer share: 65.84%

\- Average recent revenue: 247.77

\- Average monthly transactions: 816.71

\- Average transaction recent ratio: 2.95

\- Average income: 75,824.82



These customers represent the largest and most active customer group.



\### Recommended Strategy



\- Customer retention

\- Loyalty programs

\- Cross-selling

\- Increasing average transaction value

\- Personalized engagement campaigns



\---



\### 2. High-Value Occasional Customers



\- Customers: 12,161

\- Customer share: 25.33%

\- Average recent revenue: 256.02

\- Average revenue per transaction: 4.15

\- Average monthly transactions: 248.66

\- Average transaction recent ratio: 1.13

\- Average income: 72,748.05



This group has substantially higher revenue per transaction but lower

transaction frequency.



\### Recommended Strategy



\- Personalized offers

\- Premium products and services

\- Targeted reactivation campaigns

\- Increasing purchase frequency

\- Cross-selling relevant high-value products



\---



\### 3. Lower-Income Customers



\- Customers: 4,243

\- Customer share: 8.84%

\- Average recent revenue: 254.10

\- Average revenue per transaction: 1.14

\- Average monthly transactions: 731.77

\- Average transaction recent ratio: 2.67

\- Average income: 5,239.01



This segment is distinguished primarily by its substantially lower reported

income profile while maintaining meaningful transaction activity.



\### Recommended Strategy



\- Value-oriented products

\- Affordable packages

\- Targeted promotions

\- Price-sensitive offers

\- Appropriate customer engagement campaigns



\---



\## Key Business Insight



The High-Value Occasional Customer segment is particularly interesting.



Although this segment has lower transaction frequency than the

High-Engagement Core Customer segment, its average revenue per transaction is

substantially higher.



This suggests an opportunity to increase purchase frequency among these

customers through personalized and premium-oriented campaigns.



\---



\## Project Outputs



The project includes visualizations showing:



\- Customer segment distribution

\- Revenue per transaction comparison across segments

\- Customer segmentation by behavioral characteristics

\- Silhouette-score evaluation for cluster selection



\### Output Figures



```text

outputs/

└── figures/

&#x20;   ├── segment-revenue-comparison.png

&#x20;   └── customer-segment-distribution.png

