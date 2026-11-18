# South African Healthcare Customer Review Analysis

## Project Overview

This project explores customer feedback relating to two South African healthcare cover providers, Bonitas Medical Fund and Affinity Health, using Python-based natural language processing (NLP).

The analysis applies Latent Dirichlet Allocation (LDA) topic modelling to identify recurring discussion themes and VADER sentiment analysis to examine patterns of positive, negative and neutral sentiment.

The objective is to demonstrate how unstructured customer feedback can be analysed to support exploratory business analysis and identify potential areas for further investigation.

## Dataset

- **Source:** *Business Reviews from different Industries*, published on Kaggle by Ashlin Darius Govindasamy.
- **Original platform:** Hello Peter.
- **Selected reviews:** 4,966.
- **Period covered:** January 2015 to December 2022.
- **Organisations:** Bonitas Medical Fund and Affinity Health.

Bonitas operates as a medical scheme, while Affinity Health offers health insurance products. The analysis therefore does not treat the organisations as directly equivalent.

Dataset source: https://www.kaggle.com/datasets/ashlingovindasamy/business-reviews-from-different-industries

## Project Objectives

1. Explore customer review characteristics and rating distributions.
2. Identify recurring discussion themes using LDA topic modelling.
3. Classify customer sentiment using VADER.
4. Evaluate the performance and limitations of the analytical methods.
5. Identify potential business applications of the findings.

## Analytical Approach

The project was developed in Python using a Jupyter Notebook.

**Exploratory Data Analysis**

The dataset was examined for missing values, duplicates, review distributions, customer ratings and review lengths.

**Topic Modelling**

LDA was applied to 4,832 reviews after excluding 134 reviews containing fewer than five cleaned words. Models with three to seven topics were evaluated using test perplexity and interpretability.

**Sentiment Analysis**

VADER was applied to all 4,966 selected reviews to classify expressed sentiment as positive, negative or neutral.

**Model Evaluation**

LDA was evaluated using test perplexity and qualitative interpretation of the identified topics. VADER classifications were compared with sentiment categories derived from customer star ratings using accuracy and macro F1-score.

## Key Findings

### Topic Modelling

Five recurring discussion themes were identified:

1. Claims and communication
2. Hospital benefits and coverage
3. Medication and pharmacy services
4. Membership and payments
5. Positive customer service

The five-topic model was retained for its practical interpretability, although the three-topic model achieved the lowest test perplexity.

### Sentiment Analysis

| Sentiment | Reviews | Percentage |
|---|---:|---:|
| Positive | 2,801 | 56.40% |
| Negative | 1,990 | 40.07% |
| Neutral | 175 | 3.52% |

Affinity Health had a higher proportion of positive sentiment classifications (71.94%) than Bonitas Medical Fund (43.59%). This difference describes the collected reviews and does not establish which organisation provides better overall service.

### Model Evaluation

- **VADER agreement with rating-derived categories:** 77.65%
- **Macro F1-score:** 0.5506
- **Classification disagreement:** 22.35%

The evaluation highlighted challenges associated with mixed sentiment, context-dependent language and the use of customer ratings as approximate reference labels.

## Business Applications

The findings suggest that healthcare cover providers could use text analytics to support:

- Monitoring recurring customer feedback themes.
- Reviewing claims and benefit communication.
- Investigating medication and membership-related experiences.
- Identifying positive customer service practices.
- Prioritising further investigation using recent customer feedback and operational records.

## Limitations

The analysis is exploratory and has several limitations:

- Reviews were voluntarily submitted and may not represent all customers.
- The dataset covers historical reviews from 2015 to 2022.
- Topic labels required subjective interpretation.
- VADER was not specifically developed for South African healthcare financing terminology.
- Star ratings were used as approximate sentiment reference labels rather than independently annotated labels.

Automated results should therefore complement, rather than replace, qualitative assessment and human judgement.

## Project Files

The Jupyter Notebook contains the Python analysis, including data preparation, exploratory analysis, topic modelling, sentiment classification and model evaluation.

The dataset is available from the original Kaggle source linked above.

## Author

Developed as part of the Programming for Data Analytics 1 module in the Postgraduate Diploma in Data Analytics.

**Focus areas:** Python, natural language processing, exploratory data analysis, topic modelling, sentiment analysis and business analytics.
