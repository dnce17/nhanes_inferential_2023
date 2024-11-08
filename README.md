# Performing Inferential Statistics on NHANES 2021-2023 Data 

## NHANES Data
* [NHANES 2021-2023](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023)

## Data Used + Links
* [Demographics](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/DEMO_L.htm)
* [Physical Activity](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/PAQ_L.htm)
* [Blood Pressure](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/BPXO_L.htm)
* [Weight](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/WHQ_L.htm)
* [Vitamin D](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/VID_L.htm)

## Project Description
This project focuses on performing basic inferential statistics on NHANES data using Python. Relationships and differences in health metrics and demographics are explored. 

Health metrics used in this project:
* sedentary time
* systolic blood pressure (BP)
* vitamin D levels
* weight 

Demographics attributes used:
* marital status
* education level
* age

## Questions Explored, Analysis Test Done, and Results
1. Is there an association between marital status (married or not married) and education level (bachelor’s degree or higher vs. less than a bachelor’s degree)?
    * **Analysis Test performed**: Chi-square
        * Marital status - categorical
        * Education level - categorical
    * **Result**: There is an association b/w marital status and education level 
2. Is there a difference in the mean sedentary behavior time between those who are married and those who are not married?
    * **Analysis Test**: T-test
        * Sedentary behavior time - continuous (quantitative)
            * dependent variable (DV)
        * Marital status - categorical
            * indepedent variable (IV)
    * **Result**: Significant difference between the groups
3. How do age and marital status affect systolic BP?
    * **Analysis Test**: Regression
        * Age - continuous (quantitative)
            * IV
        * Marital status - categorical
            * IV
        * Systolic BP - continuous (quantitative)
            * DV
    * **Result**: Both are statistically significant and thus, affects systolic BP. However, age has a stronger effect on systolic BP than marital status.
4. Is there a correlation between self-reported weight and minutes of sedentary behavior?
    * **Analysis Test**: Correlation
        * Weight - continuous (quantitative)
        * Sedentary behavior time - continuous (quantitative)
    * **Result**: Weak correlation between the two variables

### Creative Analysis
**Instruction**: Develop your own unique question using at least one of the variables listed above. Ensure that your question can be answered using one of the following tests: chi-square, t-test, ANOVA, or correlation. Clearly state your question, explain why you chose the test, and document your findings. 

5. Is there a difference in the sedentary behavior time of those who have adequate vitamin D levels vs those who do not?
    * **Analysis Test**: T-test
        * Mean sedentary behavior time - continuous (quantitative)
            * DV
        * Vitamin D - categorical
            * IV
    * T-test is used for this question b/c there is a categorical variable with exactly 2 levels (those with and without adequate vitamin D levels) and a quantitative variable. T-test works on these variables types. 
    * **Result**: No significant difference between sedentary behavior time and those with and without adequate vitamin D levels

## Note regarding analysis
* Much of the data cleaning involves converting SEQN (participant unique identifer) to a str/obj, which is needed to merge various data together for analysis.