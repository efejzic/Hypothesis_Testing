# Hypothesis Testing Independent Simple Random Samples

**Introduction**

This analysis will focus on analyzing hemoglobin data on 500 children with iron deficiency anemia and 500 apparently healthy children (HEMOGLOB). An independent simple random sample of size 80 from each of these populations will be selected for analysis using R.

**Objectives**

The objective of this analysis is to perform appropriate outlier detection and elimination for each of the two samples and to find out if the sample data provides sufficient evidence to indicate that the two populations differ with respect to mean Hb value where α = .05. Inferential statistics using sample-based results for mean, proportion, difference in means, and difference in proportion is utilized to come to a conclusion regarding a population parameter of interest based on a single sample of 80 from the population and one sample from each population to calculate for difference in means or proportions.

**Data Description of Variables** – _Observed values with our interpretation of the data:_

![Screenshot 2024-02-04 211435](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/804102dd-0f42-4d52-8dc1-74ed1f1c4181)

**Data**
**File name:** LDS_C07_HEMOGLOB

o Variables A and HB_A will be sampled first and then independent variables B and HB_B as these are independent populations. The SRS of 80 that will be used for analysis are given a column and named as Hb_A_S and Hb_B_S.

![Screenshot 2024-04-03 144457](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/25e1f4f4-8cf5-47c6-be4e-6ff152aad300)

![Screenshot 2024-04-03 144520](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/63515de8-ffb3-4408-9cc2-55d6568415ed)

![Screenshot 2024-04-03 144539](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/edbff064-9a3e-440c-b3b7-ffa27c6c011a)

**Results and Discussion**

It is assumed that the results of the initial analysis will fail to reject the null hypothesis (where all data values come from the same normal population).

🔸🔹 Descriptive Statistics 🔹🔸

LDS_C07_HEMOGLOB

**_Population Hb_A_S_**

	Min. 1st Qu.  Median    Mean 3rd Qu.    Max.
	
	2.600   5.575   6.900   7.275   8.025  50.000
	
	vars  	  n  mean  sd  skew  kurtosis se   IQR  Q0.25  Q0.5 Q0.75
 
	X1    1 80  7.28  5.16  7.05  55.68  0.58  2.45  5.57  6.9  8.03

o The mean for SRS of 80 for population Hb_A_S (hemoglobin levels for children with anemia) is 7.275 g/dL, greater than the median of 6.900 g/dL. The IQR is 2.45 g/dL (Q3 is 8.025 – Q1 is 5.575). The 25th percentile is 5.57 g/dL, 50th percentile is 6.9 g/dL and 75th percentile is 8.03 g/dL. The range is 47.5 g/dL, where max is 50 g/dL and min is 2.600 g/dL. The standard deviation is 5.16 and the standard error is 0.58.

o	The 95 percent confidence interval for mean falls between 6.126074 and 8.423926

o	The 95 percent confidence interval for median falls between  6.2975 and 7.3

o	The 95 percent confidence interval for standard deviation falls between 1.619914 and 8.498653

**_Population Hb_B_S_**

	Min. 1st Qu.  Median    Mean 3rd Qu.    Max.
	
	2.40   11.85   12.90   12.77   14.00   16.90 
	
	vars  	  n  mean  sd  skew  kurtosis se   IQR  Q0.25  Q0.5 Q0.75
 
	X1    1 80 12.77 1.97  -1.74   7.66  0.22 2.15  11.85  12.9  14

o	The mean for SRS of 80 for population Hb_B_S (hemoglobin levels for children without anemia) is 12.77 g/dL, slightly less than the median of 12.90 g/dL. The IQR is 2.15 g/dL (Q3 is 14 – Q1 is 11.85). The 25th percentile is 11.85 g/dL, the 50th percentile is 12.9 g/dL and the 75th percentile is 14 g/dL. The range is 14.5 g/dL , where max is 16.90 g/dL and min is 2.40 g/dL. The standard deviation is 1.97 and that standard error is 0.22. 

o	The 95 percent confidence interval for mean falls between 12.32976  and 13.20774

o	The 95 percent confidence interval for median falls between 12.4 and 13.55125

o	The 95 percent confidence interval for standard deviation falls between 1.439648 and 2.398305

o	When comparing population Hb_A_S and population Hb_B_S (outliers included), where n=80, the mean for population A is less than population B (7.275 g/dL  < 12.77 g/dL), but with greater standard deviation (5.16 g/dL  > 1.97 g/dL) and greater range (47.5 g/dL   > 14.5 g/dL). This suggests that children with anemia have lower hemoglobin levels than children without anemia. The higher standard deviation and range in population Hb_A_S indicates greater variability in the hemoglobin levels among children with anemia than in children without anemia.


🔸🔹 Graphic Representations 🔹🔸

### _Histogram_

o	For SRS of 80, population Hb_A_S has an observable outlier of 50 g/dL as calculated by the initial Grubbs test. The skewness is positive at 7.05 and heavily distributed to the right towards a concentration of data with low values and few extremely high values. Kurtosis is a high positive value of 55.68 and is indicative of extreme values or outliers and a sharp peak.

**_Population Hb_A_S_**

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/419fd5b4-e169-4e79-9cfb-38ad245dafe5)

o	For SRS of 78 for population Hb_A_S with highest value outlier of 50 g/dL **removed**:

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/553cdf0f-8923-4f51-8204-e89e1721dbec)

	vars  	  n  mean  sd  skew  kurtosis se   IQR  Q0.25  Q0.5 Q0.75
 
	X1 1  78 6.73  1.83  0.12  0.14   0.21 2.45  5.53   6.9  7.97

o	The SRS for this new population is 78. After the removal of the highest outlier of 50 g/dL, we can observe more variability within the distribution of values relative to each other in the histogram for population Hb_A_S. We have failed to reject the null hypothesis after the outlier was removed, so all values fall within normal data bounds and there are no extremes.
o	The new mean is 6.73 g/dL, the standard deviation is now 1.83 and the IQR is 2.45 g/dL. Q3, or the 75th percentile, is 7.97 g/dL and Q1, or the 25th percentile, is 5.53 g/DL. The skewness is a positive value of 0.12 with a slight distribution to the right tail. The kurtosis has a positive value of 0.14 which indicates slightly heavier tails (more data points spread out) suggesting a more leptokurtic shape than a normal distribution. There is greater variability within values in the tails with fewer values close to the mean. 

**_Population Hb_B_S_**

o	For SRS of 80, population Hb_B_S has an observable outlier of 2.4 g/dL as calculated by the initial Grubbs test. The skewness is negative at -1.74 and distributed to the left with a concentration of data towards higher values with few extremely low values. Kurtosis is a positive value of 7.66, a leptokurtic distribution, with a probability of extreme values or outliers.

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/e88687cb-f9c3-44a4-b6f7-40c0a41b37fd)

o	For SRS of 78 for population Hb_B_S with lowest value outlier of 2.4 **removed:**

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/34ab1a0c-11a5-44e5-abf3-c5cde8638924)

	vars  	  n  mean  sd  skew  kurtosis se   IQR  Q0.25  Q0.5 Q0.75
 
	X1 1  78 12.88 1.59 -0.08 -0.33   0.18 2.05  11.9 12.9 13.95

o	The SRS for this new population is 78. After the removal of the lowest outlier of 2.4 g/dL, the histogram for population Hb_B_S does not reflect any extreme values. We have failed to reject the null hypothesis after the outlier was removed, so all values fall within normal bounds.
o	The new mean is 12.88 g/dL, the standard deviation is now 1.59 and the IQR is 2.05 g/dL. Q3, or the 75th percentile, is 13.95 g/dL and Q1, or the 25th percentile, 11.9 g/dL. The skewness is a negative value of -0.08 indicating a distribution skewed slightly left with a longer tail that is pulled by a few lower values. The kurtosis has a negative value of -0.33 which indicates lighter tails, with fewer values in the tails and more values close to the mean and reflects a flatter or platykurtic shape more than a normal distribution.

**_Population Hb_A_S and Hb_B_S side by side_**

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/d65ae27c-98e6-472e-b105-bb3de3556ee0)

o	Looking at both sampled populations side by side, the outliers immediately stand out with the highest value of 50 g/dL for group Hb_A_S and lowest value of 2.4 g/dL for group Hb_B_S. The values for Hb_A_S are concentrated from 0-15 g/dL along the x-axis and for Hb_B_S are concentrated primarily around 10-20 g/dL along the x-axis.

o	Histogram for populations Hb_A_S and Hb_B_S **without** outliers:

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/72508f5e-9f62-41ed-8c6d-38827c4cf8a6)


o	The extreme outliers that are the highest value of 50 g/dL and lowest value of 2.4 g/dL were removed from population Hb_A_S and Hb_B_S, respectively, and the side-by-side histogram reflects a relatively normal range of values. We can clearly observe from the histogram that population A, hemoglobin levels of children with anemia reflect more values with lower grams per deciliter (g/dL) which is used to measure the concentration of hemoglobin in blood.  

### _Box Plots_

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/549af74c-728a-4de4-8358-72dff70c50a5)

o	Looking at both sampled populations, group Hb_A_S does not have many values over 10 g/dL, with the extreme exception of high-value outlier, 50 g/dL. IQR is 2.45 g/dL. The 25th percentile is 5.57 g/dL, 50th percentile is 6.9 g/dL and 75th percentile is 8.03 g/dL. Group Hb_B_S value points often reach over 10 g/dL, except for an extremely low-value outlier of 2.4 g/dL. IQR is 2.15 g/dL. The 25th percentile is 11.85 g/dL, the 50th percentile is 12.9 g/dL and the 75th percentile is 14 g/dL.

o	Box plot for populations Hb_A_S and Hb_B_S **without** outliers.

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/bcb61535-191b-43b9-8048-e28a23673b8a)

o	Population Hb_A_S has an interquartile range of 2.45 g/dL. Q3, or the 75th percentile, is 7.97 g/dL and Q1, or the 25th percentile, is 5.53 g/dL. This indicates that the middle 50% of data falls within the range of 7.97 g/dL and 5.53 g/dL. Population Hb_B_S has an interquartile range of 2.05 g/dL. Q3, or the 75th percentile, is 13.95 g/dL and Q1, or the 25th percentile, is 11.9 g/dL. This indicates that the middle 50% of data falls within the range of 13. 95 g/dL and 11.9 g/dL. Additionally, 25% of the population of Hb_A_S has values less than or equal to 5.53 g/dL while 25% of the population for Hb_B_S has values less than or equal to 11.9 g/dL.

### _Scatter Plots_

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/4ccf9884-e4af-498e-bd7a-aba2030cbf4b)

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/d3934a21-9cdd-441d-816c-1b45a02a3dd1)

o	The scatterplot for population Hb_A_S illustrates that most values are concentrated under 10 g/dL with one abnormal outlier at 50 g/dL. The scatterplot for population Hb_B_S illustrates that most values are concentrated between 10 g/dL and 15 g/dL with one value on the extreme lower end at 2.4 g/dL.

o	Population outliers **excluded:**


	Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
	
	2.600   5.525   6.900   6.727   7.975  11.900 
	
	Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
 
	9.30   11.90   12.90   12.88   13.95   16.90 

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/7e5403e2-99f3-4b7d-9480-9dc196d33aa3)

o	The scatterplot for population Hb_A_S is reflected without the highest value outlier of 50 g/dL. There is greater visible variability and spread within the data points. The highest value within the data points is now 11.9 g/dL. The lowest is 2.60 g/dL and the range is 9.3 g/dL. The median is 6.9 g/dL close to the mean if 6.727 g/dL.

![image](https://github.com/efejzic/Hypothesis_Testing/assets/119814593/78b77aa4-b6d2-48f0-af26-1b950d0269b3)

o	The scatterplot for population Hb_B_S is reflected without the lowest value outlier of 2.4 g/dL. The data is visibly more evenly distributed. The highest value is now 16.90 g/dL, and the lowest value is 9.30 g/dL. The range is 7.6 g/dL. The median is 12.90 g/dL, close to the mean of 12.88 g/dL.

### _Grubbs Test_

LDS_C07_HEMOGLOB

o	The Grubbs test is used to identify a single outlier within a dataset. 

o	**G** – the test statistic where a larger value indicates stronger deviation from the mean.

o	**U** –  critical value based on the significance level of 0.05

**Outlier Test: Hb_A_S, Hb_B_S**

Method 

	Null hypothesis – All data values come from the same normal population
	
	Alternative hypothesis – Smallest or largest value is an outlier
	
	Significance level: α = 0.05

**_Population Hb_A_S_**

_First test_

Grubbs test for one outlier

	data:  Hb_A_S
	
	G = 8.27554, U = 0.12213, p-value < 2.2e-16
	
	alternative hypothesis: highest value 50 is an outlier

o	For an SRS count of 80, the Grubbs test has identified the highest value of 50 g/dL as an outlier for population Hb_A_S. The p value of < 2.2e-16 is significantly smaller than the significance level of 0.05, showing evidence against the null hypothesis. The G value (8.27554) is much larger than the U value (0.12213) and far enough to be considered statistically significant. The first test results go against the initial assumption that we will fail to reject the null hypothesis. A second Grubbs’ test will be done after the removal of the highest value.

_Second test_

Removal of highest outlier – 50

Grubbs test for one outlier

	data:  HEMOGLOB_SRS80_filtered$Hb_A_S_no_outliers
	
	G = 2.84492, U = 0.89491, p-value = 0.1407
	
	alternative hypothesis:highest value 11.9 is an outlier

o	The results of the Grubbs test after removing the highest value of 50 g/dL now reflect the highest value as 11.9 g/dL as an outlier, which will be left alone as that falls within bounds for the rest of the data points. The G value (2.84492), critical value U (0.89491) and p value is 0.1407. The G value is not far enough from the U value to be considered statistically significant in this test. In addition, the p value of 0.1407 is greater than the significance level of 0.05. Based on the data, we fail to reject the null hypothesis.

**_Population Hb_B_S_**

_First test_

Grubbs test for one outlier

	data:  Hb_B_S
	
	G = 5.25629, U = 0.64584, p-value = 2.331e-07
	
	alternative hypothesis: lowest value 2.4 is an outlier

o	For an SRS count of 80, the Grubbs’ test has identified the lowest value of 2.4 g/dL as an outlier of population Hb_B_S. The p value of 2.331e-07 is significantly smaller than the significance level of 0.05, so this shows evidence against the null hypothesis. The G value (5.25629) is high compared to the U value (0.64584), further supporting that 2.4 g/dL is an outlier and showing evidence against the null hypothesis. A second Grubbs’ test will be done after the removal of the lowest value.

_Second test_

Removal of lowest outlier – 2.4

	data:  :  HEMOGLOB_SRS80_filtered$Hb_B_S
	
	G = 2.50717, U = 0.91838, p-value = 0.4227
	
	alternative hypothesis: highest value 16.9 is an outlier

o	The results of the Grubbs test after removing the lowest value of 2.4 g/dL now reflect the highest value as 16.9 g/dL as an outlier, which will be left alone as that falls within bounds for the rest of the data points. The G value (2.50717), critical value U (0.91838) and p value is 0.4227. The G value is not far enough from the U value to be considered statistically significant in this test. In addition, the p value of 0.4227 is greater than the significance level of 0.05. Based on the data, we fail to reject the null hypothesis.

### _95 percent CI: Hb_A_S and Hb_B_S - Outliers **excluded:**_

LDS_C07_HEMOGLOB

**_Population Hb_A_S_**

	[1] 6.315132 7.138714
	
	attr(,"conf.level")
	
	[1] 0.95

o	The population size is an SRS of 78. We are 95% confident that the true population mean for population Hb_A_S after the removal of the highest value of 50 g/dL lies within the interval 6.315 g/dL and 7.138 g/dL. The calculated mean is 6.73.
 
**_Population Hb_B_S_**

	[1] 12.51789 13.23596
	
	attr(,"conf.level")
	
	[1] 0.95
 
o	The population size is an SRS of 78. We are 95% confident that the true population mean for population Hb_B_S after the removal of the lowest value of 2.4 g/dL lies within the interval 12.517 g/dL and 13.235 g/dL. The calculated mean is 12.88.

### _Two-Sample T-Test and CI: Hb_A_S, Hb_B_S_

LDS_C07_HEMOGLOB

Welch Two Sample t-test data: 

•	We are using a Welch two sample t-test to compare the means of two independent groups because the population variance is unknown.

	Welch Two Sample t-test
	
	data:  HEMOGLOB_SRS80_filtered$Hb_A_S_no_outliers and HEMOGLOB_SRS80_filtered$Hb_B_S

	t = -22.415, df = 151.19, p-value < 2.2e-16
	
	alternative hypothesis: true difference in means is not equal to 0
 	
	95 percent confidence interval: -6.692086 -5.607914
	
	sample estimates: mean of x 6.726923 mean of y 12.876923 

o	The population size is an SRS of 78. We are 95% confident that the difference between population means is somewhere between -6.692 and -5.607. The interval does not include zero. If we were to repeat the study many times and compute confidence intervals in the same, about 95 percent of the intervals would include the difference between the population means. The t statistic of -22.415 is negative which suggests the sample mean is lower than the hypothesized population mean. The degrees of freedom or df is 151.19. The p value of < 2.2e-16 is extremely small and below the significance level of 0.05, suggesting strong evidence against the null hypothesis in addition to the interval not including zero. There is a significant difference between the means of the two groups.


### Age-Based Hemoglobin Levels in Children and Adolescents

_The mean hemoglobin level for with a -2 standard deviation:_

6 months to 2 years: 12 g/dL to 10.5 g/dL

2 to 6 years: 12.5 g/dL to 11.15 g/dL

6 to 12 years: 13.5 g/dL to 11.5 g/dL

12 to 18 years 

**Males:** 14.5 g/dL to 13 g/dL

**Females:** 14 g/dL to 12 g/dL

Wang. M. (2016). Iron Deficiency and Other Types of Anemia in Infants and Children. American Family Physician. 15;93(4) PMID: 26926814

### **Conclusion**

Population Hb_A_S indicates hemoglobin levels of children with anemia and population Hb_B_S indicates hemoglobin levels of children without anemia. It is assumed that the results of the initial analysis with a SRS of 80 will fail to reject the null hypothesis (where all data values come from the same normal population). The initial analysis which was performed including the highest value outlier of 50 g/dL for population Hb_A_S and lowest value 2.4 g/dL for population Hb_B_S produced strong evidence against the null hypothesis, rendering the initial assumption wrong. For an SRS count of 80, the Grubbs test indicated the outliers, test statistic and critical value for both populations. Population Hb_A_S had a p value of < 2.2e-16, significantly smaller than the significance level of 0.05, and population Hb_B_S had a p value of 2.331e-07, also significantly smaller than the significance level of 0.05, both showing evidence against the null hypothesis. The G value (8.27554) is much higher than the U value (0.12213) indicating the highest value of 50 g/dL as statistically significant and an outlier for Hb_A_S. For population Hb_B_S, the G value (5.25629) is much higher than the U value (0.64584) as well, reaching the same conclusion that 2.4 g/dL is statistically significant and an outlier.

A chart depicting normal hemoglobin levels in children and adolescents is shown above. The new assumption for the SRS of 78 (after the removal of outliers) is that we will fail to reject the null hypothesis. The decision to remove the highest and lowest value outliers was to ensure quality of the dataset and decrease influence of extreme observations that can distort assumptions. The highest value of 50 g/dL for population Hb_A_S is extremely abnormal and thus not considered relevant to the rest of the dataset while the lowest value 2.4 g/dL is possible clinically, but I decided to remove it to represent more accuracy overall for population Hb_B_S.  A second Grubbs test was conducted for both populations after the outliers were removed. Based on the data for population Hb_A_S in the second test, we fail to reject the null hypothesis as the p value of 0.1407 is greater than the significance level of 0.05. The G value (2.84492) is greater than the critical value U (0.89491), however, when compared to the original Grubbs test for this population, I used discretion to determine to include the next highest value of 11.9 as relevant to the rest of the datapoints and clinically sound. Based on the data for population Hb_B_S, we fail to reject the null hypothesis as the p value of 0.4227 is greater than the significance level of 0.05. The G value (2.50717) is greater than the critical value U (0.91838), however, as with population Hb_A_S, we fail to reject the null hypothesis as the new outlier of 16.9 is statistically relevant with the rest of the datapoints.

The assumption for the Welch two sample t test results for SRS 78 is that the means of the two populations (6.727 g/dL for population Hb_A_S and 12.88 g/dL for population Hb_B_S) after the removal of outliers are statistically significant, rejecting the null hypothesis. The t test was done to compare the means of two independent groups when population variances are unknown. We are 95% confident that the difference between population means is somewhere between -6.692 and -5.607, where the interval does not include zero. This supports the conclusion that there is a statistically significant difference between the means of the two populations. The mean hemoglobin levels for children with anemia are smaller than the mean hemoglobin levels for children without anemia. The Central Limit Theorem states that the sampling distribution of a sample mean is approximately normal if the sample size is large enough, even if the population is not normal (Zach, 2019). We can assume that the means of the two populations are normally distributed in the context of the Welch two sample t-test. The negative t-statistic of -22.415 suggests a significant difference in means, but the use of a large sample size as supported by the assumption of normality by the CLT, can enhance the credibility of our statistical conclusion.




