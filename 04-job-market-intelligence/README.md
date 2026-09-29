# 💼 Job Market & Career Intelligence

## Overview

This project analyzes **15,841 Analytics job listings** and **1,602 Data Science job records** to identify hiring patterns, in-demand skills, experience requirements, salary patterns, and broader career-market signals.

The project combines exploratory data analysis, feature engineering, skill intelligence, job-demand analysis, salary-band classification, and machine learning into a structured career-intelligence workflow.

## Business Objective

The analysis is designed to help understand:

- Which roles have strong observed demand
- Which companies show substantial hiring activity
- Which skills appear frequently in job listings
- How observed salary patterns vary across roles
- How experience requirements relate to salary
- Which skills are associated with different career paths
- Whether job-market attributes contain useful information for distinguishing observed salary bands

## Datasets

### Analytics Jobs — 15,841 records

Key fields include:

- Experience
- Job description
- Job designation
- Job type
- Key skills
- Location
- Salary

### Data Science Jobs — 1,602 records

Key fields include:

- Company
- Job title
- Minimum experience
- Average salary
- Minimum salary
- Maximum salary
- Number of jobs

The datasets are analyzed separately because they have different schemas and represent different levels of job-market information.

## Workflow

```text
Raw Job Data
    ↓
Data Cleaning
    ↓
Feature Engineering
    ↓
Exploratory Data Analysis
    ↓
Skill Demand Analysis
    ↓
Skill + Salary Analysis
    ↓
Skill & Role Intelligence
    ↓
Job Demand & Salary Intelligence
    ↓
Salary Band Classification
    ↓
Model Comparison
    ↓
Career Intelligence Engine
```

## Machine Learning

The project builds a salary-band classification workflow using job designation, location, key skills, and minimum experience as model features.

The final notebook reports:

- Training rows: 12,672
- Testing rows: 3,169
- Random Forest accuracy: 0.3613
- Random Forest macro F1: 0.3575

These metrics should be interpreted as model-evaluation results on this dataset, not as a general salary-prediction guarantee.

## Outputs

The project includes six final figures:

1. Top Analytics roles
2. Top Data Science companies
3. Top Analytics skills
4. Job demand vs. average salary
5. Salary-band model performance
6. Salary-model feature importance

## Reproducibility

The notebook uses project-relative paths for the bundled datasets and output figures, so it can be run from the project directory without relying on a machine-specific Windows path.

Install dependencies with:

```bash
pip install -r requirements.txt
```

Then open:

```text
notebooks/01_job_market_and_career_intelligence.ipynb
```

## Limitations

- The datasets represent observed job-market records and should not be treated as a complete real-time view of the market.
- Salary values are dataset-derived estimates and can vary by source, location, role, and experience.
- Classification performance is dataset-specific.
- Career insights are descriptive and analytical rather than guarantees about future hiring or compensation.
