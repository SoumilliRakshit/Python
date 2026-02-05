# Topic 1- Probability Essentials

## 1. What is Probability?
Probability is a numerical measure of the likelihood that an event will occur.  
It ranges between **0 and 1**, where:
- `0` → impossible event  
- `1` → certain event  

**Formula (Classical Probability):**
\[
P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}
\]

---

## 2. Basic Terminology

- **Experiment**: A process with a well-defined outcome  
  *Example: Tossing a coin*

- **Sample Space (S)**: Set of all possible outcomes  
  *Example: S = {H, T}*

- **Event (E)**: A subset of the sample space  
  *Example: Getting a head*

- **Outcome**: A single result of an experiment

---

## 3. Types of Events

- **Simple Event**: Contains only one outcome  
- **Compound Event**: Contains more than one outcome  

- **Certain Event**: Event that always occurs  
- **Impossible Event**: Event that never occurs  

- **Mutually Exclusive Events**: Events that cannot occur together  
  \[
  A \cap B = \emptyset
  \]

- **Exhaustive Events**: Events that cover all possible outcomes  

---

## 4. Axioms of Probability

1. \( P(A) \ge 0 \) for any event A  
2. \( P(S) = 1 \)  
3. If A and B are mutually exclusive:  
   \[
   P(A \cup B) = P(A) + P(B)
   \]

---

## 5. Complement of an Event

The complement of event A (denoted by \( A' \)) includes all outcomes not in A.

\[
P(A') = 1 - P(A)
\]

---

## 6. Addition Rule of Probability

### Case 1: Mutually Exclusive Events
\[
P(A \cup B) = P(A) + P(B)
\]

### Case 2: Non–Mutually Exclusive Events
\[
P(A \cup B) = P(A) + P(B) - P(A \cap B)
\]

---

## 7. Conditional Probability

Conditional probability measures the probability of event A given that event B has occurred.

\[
P(A|B) = \frac{P(A \cap B)}{P(B)}, \quad P(B) \neq 0
\]

---

## 8. Multiplication Rule

### General Rule
\[
P(A \cap B) = P(A) \cdot P(B|A)
\]

---

## 9. Independent Events

Two events A and B are independent if:
\[
P(A \cap B) = P(A) \cdot P(B)
\]

or
\[
P(A|B) = P(A)
\]

---

## 10. Bayes’ Theorem

Bayes’ theorem helps revise probabilities based on new information.

\[
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
\]

---

## 11. Random Variables

A **random variable** assigns a numerical value to each outcome of an experiment.

- **Discrete Random Variable**: Takes countable values  
- **Continuous Random Variable**: Takes values over an interval  

---

## 12. Probability Distribution

A probability distribution describes how probabilities are distributed over values of a random variable.

### Discrete Probability Distribution Properties:
- \( 0 \le P(X=x) \le 1 \)
- \( \sum P(X=x) = 1 \)

---

## 13. Mean (Expected Value)

\[
E(X) = \sum x \cdot P(X=x)
\]

---

## 14. Variance and Standard Deviation

### Variance
\[
Var(X) = E(X^2) - [E(X)]^2
\]

### Standard Deviation
\[
\sigma = \sqrt{Var(X)}
\]

---

## 15. Common Probability Distributions

- **Bernoulli Distribution**
- **Binomial Distribution**
- **Poisson Distribution**
- **Normal Distribution**

---

## 16. Key Takeaways

- Probability quantifies uncertainty  
- Events can be dependent or independent  
- Conditional probability is central to real-life decision making  
- Bayes’ theorem updates beliefs with new evidence  

---

# Tppic 2- Data Cleaning and Pre-processing

## 1. What is Data Cleaning and Pre-processing?
Data cleaning and pre-processing refer to the steps taken to **prepare raw data** for analysis or modeling.  
Real-world data is often **incomplete, inconsistent, noisy, or unstructured**, making pre-processing essential.

**Goal:** Improve data quality to ensure accurate analysis and reliable results.

---

## 2. Importance of Data Pre-processing

- Improves data accuracy and consistency  
- Reduces errors and bias in analysis  
- Enhances model performance  
- Saves time during analysis  
- Ensures meaningful insights from data  

---

## 3. Types of Data Issues

### 3.1 Missing Data
Occurs when values are absent in one or more variables.

**Causes:**
- Data entry errors  
- Non-response in surveys  
- System failures  

---

### 3.2 Noisy Data
Data containing random errors or outliers.

**Examples:**
- Typographical errors  
- Measurement errors  

---

### 3.3 Inconsistent Data
Data with conflicting or illogical values.

**Examples:**
- Age = −5  
- Different date formats in the same column  

---

### 3.4 Duplicate Data
Repeated records that distort analysis.

---

## 4. Handling Missing Data

### Common Techniques:
- **Deletion**
  - Remove rows or columns with missing values  
- **Mean/Median/Mode Imputation**
- **Forward or Backward Fill**
- **Predictive Imputation**
  - Using regression or machine learning models  

---

## 5. Handling Noisy Data

- **Smoothing techniques**
- **Binning**
- **Outlier detection and removal**
- **Data transformation**

---

## 6. Handling Inconsistent Data

- Standardizing formats (dates, units, text)  
- Correcting logical inconsistencies  
- Cross-checking with domain knowledge  

---

## 7. Data Transformation

Data transformation converts data into a suitable format for analysis.

### Common Techniques:
- **Normalization**
- **Standardization**
- **Log Transformation**
- **Encoding categorical variables**

---

## 8. Data Normalization

Scales numerical values to a fixed range (usually 0 to 1).

\[
X' = \frac{X - X_{min}}{X_{max} - X_{min}}
\]

**Used when:** Features have different scales.

---

## 9. Data Standardization

Centers data around the mean with unit variance.

\[
Z = \frac{X - \mu}{\sigma}
\]

**Used when:** Data follows a normal distribution.

---

## 10. Encoding Categorical Data

### Common Methods:
- **Label Encoding**
- **One-Hot Encoding**
- **Ordinal Encoding**

---

## 11. Data Integration

Combining data from multiple sources into a unified dataset.

**Challenges:**
- Schema mismatches  
- Redundant attributes  
- Conflicting data values  

---

## 12. Data Reduction

Reduces data size while preserving important information.

### Techniques:
- Feature selection  
- Feature extraction  
- Dimensionality reduction (e.g., PCA)  

---

## 13. Data Discretization

Converts continuous data into categorical intervals.

**Examples:**
- Age → Young, Adult, Senior  
- Income → Low, Medium, High  

---

## 14. Data Pre-processing Workflow

1. Data Collection  
2. Data Cleaning  
3. Handling Missing Values  
4. Data Transformation  
5. Data Reduction  
6. Final Dataset for Analysis  

---

## 15. Tools Used for Data Cleaning

- Microsoft Excel  
- Python (Pandas, NumPy)  
- R  
- SQL  
- Power BI / Tableau  

---

## 16. Key Takeaways

- Data cleaning is a crucial step before analysis  
- High-quality data leads to reliable insights  
- Pre-processing improves efficiency and accuracy  
- Most real-world data requires extensive cleaning  

---

📌 *Tip:* Always explore and understand data before applying pre-processing techniques.



📌 *Tip:* Use examples and Venn diagrams to strengthen understanding.


# Topic 3- Ordinary Least Squares (OLS) and Normal Equations

## 1. What is Ordinary Least Squares (OLS)?
Ordinary Least Squares (OLS) is a method used to estimate the parameters of a **linear regression model** by minimizing the **sum of squared residuals**.

In Economics, OLS is the backbone of **empirical analysis**, policy evaluation, and causal inference.

---

## 2. Linear Regression Model

### Simple Linear Regression
\[
Y_i = \beta_0 + \beta_1 X_i + \varepsilon_i
\]

### Multiple Linear Regression
\[
Y_i = \beta_0 + \beta_1 X_{1i} + \beta_2 X_{2i} + \cdots + \beta_k X_{ki} + \varepsilon_i
\]

Where:
- \( Y_i \) = dependent variable  
- \( X_{ki} \) = independent variables  
- \( \beta_k \) = parameters to be estimated  
- \( \varepsilon_i \) = error term  

---

## 3. Objective of OLS

OLS chooses parameter estimates that minimize:

\[
\min_{\beta} \sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2
\]

This ensures the **best linear fit** to the data.

---

## 4. Residuals

\[
e_i = Y_i - \hat{Y}_i
\]

Properties of OLS residuals:
- Sum of residuals equals zero
- Residuals are orthogonal to regressors

---

## 5. Matrix Representation of the Model

\[
\mathbf{Y} = \mathbf{X}\beta + \varepsilon
\]

Where:
- \( \mathbf{Y} \) is an \( n \times 1 \) vector
- \( \mathbf{X} \) is an \( n \times k \) matrix (including intercept)
- \( \beta \) is a \( k \times 1 \) vector
- \( \varepsilon \) is an \( n \times 1 \) vector

---

## 6. The Normal Equations

To minimize the sum of squared errors, we set the first derivative equal to zero:

\[
\mathbf{X}'(\mathbf{Y} - \mathbf{X}\beta) = 0
\]

This yields the **Normal Equations**:

\[
\mathbf{X}'\mathbf{X}\beta = \mathbf{X}'\mathbf{Y}
\]

---

## 7. OLS Estimator

Provided \( \mathbf{X}'\mathbf{X} \) is invertible:

\[
\hat{\beta} = (\mathbf{X}'\mathbf{X})^{-1} \mathbf{X}'\mathbf{Y}
\]

This is the **OLS estimator**.

---

## 8. Conditions for Existence of OLS Estimator

- No perfect multicollinearity  
- Full column rank of \( \mathbf{X} \)  
- Number of observations \( n > k \)

---

## 9. Assumptions of the Classical Linear Regression Model (CLRM)

1. Linearity in parameters  
2. Random sampling  
3. No perfect multicollinearity  
4. Zero conditional mean:
   \[
   E(\varepsilon | X) = 0
   \]
5. Homoskedasticity:
   \[
   Var(\varepsilon | X) = \sigma^2
   \]

---

## 10. Gauss–Markov Theorem

Under CLRM assumptions, the OLS estimator is the **Best Linear Unbiased Estimator (BLUE)**.

---

## 11. Interpretation of OLS Coefficients

- \( \beta_k \) measures the **ceteris paribus** effect of \( X_k \) on \( Y \)
- In log-linear models, coefficients represent **elasticities**

---

## 12. Variance of OLS Estimator

\[
Var(\hat{\beta}) = \sigma^2 (\mathbf{X}'\mathbf{X})^{-1}
\]

Estimated using:
\[
\hat{\sigma}^2 = \frac{1}{n - k} \sum e_i^2
\]

---

## 13. Hypothesis Testing in OLS

- **t-tests** for individual coefficients
- **F-tests** for joint significance
- Confidence intervals for parameters

---

## 14. Goodness of Fit

### R-squared
\[
R^2 = 1 - \frac{SSR}{SST}
\]

Measures the proportion of variance explained by the model.

---

## 15. OLS in Economic Applications

Common uses:
- Estimating demand and supply
- Wage and income analysis
- Policy impact evaluation
- Growth and development studies

---

## 16. Limitations of OLS

- Sensitive to outliers
- Cannot handle endogeneity
- Assumes linearity
- Biased under omitted variable bias

---

## 17. OLS and Causal Inference

OLS estimates causal effects **only if**:
- Regressors are exogenous
- No omitted variable bias
- No reverse causality

Otherwise, methods like **IV, DiD, RDD** are required.

---

## 18. Key Takeaways

- OLS minimizes squared residuals
- Normal equations lead to closed-form solutions
- Assumptions determine validity
- Interpretation matters as much as estimation

