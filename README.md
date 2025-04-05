# Environmental Impact of Food Production Analysis
The Environmental Impact of Food Production Analysis project focuses on dissecting the various environmental impact of food production, with an emphasis on key metrics such as carbon emissions, water usage, and land use.


## 1. Business Understanding
#### 📌 Project Objective

The goal of this project is to assess the environmental impact of food production at both macro and micro levels and propose data-driven insights to mitigate the negative effects of food production on the environment. This will help policymakers, environmentalists, food producers, and consumers make more informed decisions that support sustainability.


Key Objectives;

1. Assess the environmental impact of different food products based on:

    * Carbon emissions

    * Water usage

    * Land use

2. Identify high-impact vs. low-impact foods.

3. Provide data-driven recommendations for sustainable food production.


**📌 Analytical Questions**

1. Which food products have the highest and lowest carbon emissions?

2. How do plant-based vs. animal-based foods compare in environmental impact?

3. What is the correlation between land use, water use, and emissions?

4. Which food production stage (farm, transport, packaging, retail) contributes most to emissions?

5. How do different food types (cereals, dairy, meat, vegetables) impact the environment?

6. What are the  five contributors to eutrophication (water pollution)?

7. Can we group foods based on their environmental impact using clustering?


**📌 Hypothesis Testing**

    - H₀ (Null Hypothesis): There is no significant difference in environmental impact between plant-based and animal-based foods.

    - H₁ (Alternative Hypothesis): Animal-based foods have a significantly higher environmental impact than plant-based foods.

### Hypothesis Testing Summary

| Metric           | U-statistic | p-value  | Result                   |
|-----------------|------------|----------|----------------------------|
| Total Emissions | 27.0000     | 1.0000   | No significant difference |
| Total Water Use | 91.0000     | 0.9840   | No significant difference |
| Total Land Use  | 59.0000     | 0.9989   | No significant difference |


## 2. Data Understanding
The dataset includes 43 food products and 23 features related to environmental impacts (such as land use, water use, and carbon footprint across production stages).

Key features:

* Greenhouse gas emissions across production stages (land use change, animal feed, transport, packaging, etc.).

* Eutrophication impact (nutrient runoff affecting water bodies).

* Water and land usage metrics.

* Breakdown of emissions at different production stages (farm, transport, packaginng, retail).


#### Exploratory Data Analysis (EDA) Insights:

* Feature distributions are right-skewed, meaning most values are concentrated at the lower end, with some extreme values.

* Potential outliers in high-impact categories such as land use and farm emissions.

* Principal Component Analysis (PCA) shows most variance is captured in the first principal component (PC1).

## 3. Data Preparation

Data preparation involved several steps to clean, transform, and structure the dataset for analysis:

1. Handling Missing Values:

    * No significant missing data were found in the dataset due to its small size.

    * Some minor inconsistencies in column names were standardized.

2. Feature Engineering:

    * Created new features like Categories, Total Environmental Impact (by summing normalized values of emissions, water usage, and land use) among others

    * Filled missing values using Median because it is less affected by Outliers and the fact that environmental factors rarely follow a normal distribution. In this case, Mean would have overestimated the central tendency and could have been skewed by very high or low values leading to inaccurate imputations. 

3. Data Quality:
    * Corrected wrongly spelt column "Packging" to "Packaging"


## 4. Modeling

Several analytical techniques were applied to derive insights:

1. Clustering Analysis (K-Means & Hierarchical Clustering)

    * Grouped foods based on their Categories (Plant-Based and Animal-Based).

2. Correlation Analysis

    * Measured relationships between land use, water use, and carbon emissions.

    * Found strong correlations between land use and emissions, suggesting significant environmental trade-offs.

3. Hypothesis Testing

    * Used Mann-Whitney U test to compare environmental impact between plant-based and animal-based foods.

        * Results showed no statistically significant difference in overall impact.

4. PCA for Dimensionality Reduction

    * Reduced feature space while retaining most of the variance.

    * Helped identify key drivers of environmental impact.

## 5. Evaluation

1. 📌 Key Findings;

    * Animal-based foods generally have higher emissions, but plant-based foods also contribute to land and water use.

    * Farm and Land Use Change contribute the most to environmental impact, while transport and packaging have lower impact.

    * High-impact foods include beef, lamb, and cheese, while low-impact foods include peas, nuts, and soy products.

    * Cluster analysis identified clear groups of foods based on environmental impact, helping prioritize sustainability efforts.


2. 📌 Limitations & Considerations:

    * Data sources may have varying levels of accuracy.

    * Impact assessment does not consider socio-economic factors like food accessibility, consumer behavior and financial cost of sustainable alternatives.


## 6. Recommendations

📌 Sustainability Recommendations

1. Policy & Regulation;

    * Implement carbon pricing on high-impact foods.

    * Support research into sustainable farming methods.

2. Consumer Awareness;

    * Promote plant-based alternatives with lower impact.

    * Develop labeling systems indicating environmental impact scores on food products.

3. Food Industry Innovations

    * Reduce land use through improved agricultural practices.

    * Optimize supply chains to cut down transportation emissions.

    * Invest in sustainable packaging solutions.


📌 Future Work

* Integrate real-time emissions tracking for food production.

* Explore machine learning models for predictive environmental impact modeling.

## 7. Deployment


## 8. Conclusion

This project provides a comprehensive analysis of the environmental impact of food production, offering data-driven insights to guide policy decisions, business strategies, and consumer choices. By leveraging data science techniques such as clustering, PCA, and hypothesis testing, we can identify high-impact foods and propose sustainable solutions for a healthier planet.

