# E-commerce-Campaign data:  EDA & Hypothesis testing with Python

🎯 Problem statement

To conduct a thorough exploratory data analysis (EDA) and hypothesis testing on two comprehensive datasets one containing information on customers visiting the shopping site for purchase and another that has demographic, purchase, and marketing information about the group of people.

## Dataset

Here is the data dictionary converted into a table format:

| **Column**              | **Description**                                                     |
|-------------------------|---------------------------------------------------------------------|
| **ID**                  | Customer's Unique Identifier                                        |
| **Year_Birth**           | Customer's Birth Year                                               |
| **Education**            | Customer's education level (Graduation, Master, PhD, Diploma, Basic)|
| **Marital_Status**       | Customer's marital status                                           |
| **Income**               | Customer's yearly household income                                  |
| **Kidhome**              | Number of children in customer's household                          |
| **Teenhome**             | Number of teenagers in customer's household                         |
| **Dt_Customer**          | Date of customer's enrollment with the company                      |
| **Recency**              | Number of days since customer's last purchase                       |
| **MntWines**             | Amount spent on wine in the last 2 years                            |
| **MntFruits**            | Amount spent on fruits in the last 2 years                          |
| **MntMeatProducts**      | Amount spent on meat in the last 2 years                            |
| **MntFishProducts**      | Amount spent on fish in the last 2 years                            |
| **MntSweetProducts**     | Amount spent on sweets in the last 2 years                          |
| **MntGoldProds**         | Amount spent on gold in the last 2 years                            |
| **NumDealsPurchases**    | Number of purchases made with a discount                            |
| **NumWebPurchases**      | Number of purchases made through the company's website              |
| **NumCatalogPurchases**  | Number of purchases made using a catalogue                          |
| **NumStorePurchases**    | Number of purchases made directly in stores                         |
| **NumWebVisitsMonth**    | Number of visits to company's website in the last month             |
| **AcceptedCmp1**         | 1 if customer accepted the offer in the 1st campaign, 0 otherwise   |
| **AcceptedCmp2**         | 1 if customer accepted the offer in the 2nd campaign, 0 otherwise   |
| **AcceptedCmp3**         | 1 if customer accepted the offer in the 3rd campaign, 0 otherwise   |
| **AcceptedCmp4**         | 1 if customer accepted the offer in the 4th campaign, 0 otherwise   |
| **AcceptedCmp5**         | 1 if customer accepted the offer in the 5th campaign, 0 otherwise   |
| **Complain**             | 1 if customer complained in the last 2 years, 0 otherwise           |
| **Country**              | Customer's location                                                 |

# steps performed

1. **Exploratory Data Analysis (EDA)**:
   - Analyzed various features like income, education, spending categories, and marital status.
   - Visualized distributions using histograms and box plots, identifying skewed features and outliers.
   - Removed extreme values (outliers) where necessary to improve the analysis.

2. **Feature Engineering**:
   - Created new features such as:
     - **Income Brackets**: Divided income into two groups (below and above median income).
     - **Couples vs. Singles**: Grouped marital statuses into "In Couple" (Married, Together) and "Alone" (Divorced, Single, Widow, YOLO, Absurd).
     - **Campaign Acceptance**: Created a binary feature indicating whether a customer accepted any campaign.

3. **Hypothesis Testing**:
   - **Income vs. Education**:
     - **Hypothesis**: Is the income of customers dependent on their education level?
     - Conducted suitable tests (Chi-square or ANOVA) to check if there's a significant relationship between income and education.
   
   - **Income vs. Total Spending**:
     - **Hypothesis**: Do higher-income individuals spend more across all categories?
     - Performed correlation analysis and t-tests to examine the relationship between income and total spending.

   - **Couples vs. Singles (Wine Spending)**:
     - **Hypothesis**: Do couples spend more or less on wine compared to people living alone?
     - Conducted t-tests or Mann-Whitney U tests to compare wine spending between "In Couple" and "Alone" groups.

   - **Income vs. Campaign Acceptance**:
     - **Hypothesis**: Are people with lower income more likely to accept campaigns?
     - Split data into two income groups and checked campaign acceptance rates using Chi-square or logistic regression tests.

4. **Assumptions and Test Selection**:
   - Selected appropriate statistical tests (e.g., t-tests, Chi-square, ANOVA) based on the type of data and hypotheses.
   - Verified normality and homogeneity of variance using visualizations (histograms, Q-Q plots) and statistical tests (Levene's, Shapiro-Wilk).
   
5. **Results and Conclusions**:
   - Derived insights and accepted or rejected null hypotheses based on p-values, summarizing the findings for each analysis.
