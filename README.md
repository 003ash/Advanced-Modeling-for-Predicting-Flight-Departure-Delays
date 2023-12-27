# Advanced-Modeling-for-Predicting-Flight-Departure-Delays

## Overview

This project aims to predict flight departure delays in the United States, offering valuable insights into the factors influencing delays in the aviation industry. By analyzing a comprehensive dataset, we explore correlations between airport busyness, airline size, airport terrain, and departure delays. Leveraging innovative techniques, including a novel neural network architecture for regression analysis and clustering-based categorical encoding, our research provides actionable insights for optimizing airline economics and enhancing passenger experiences.

The detailed report can be found here: [Link to report](https://github.com/003ash/Advanced-Modeling-for-Predicting-Flight-Departure-Delays/blob/main/CSE_519_Final_Report.pdf)

## Novel Key Features

- **Categorical Encoding:** Our unique clustering-based categorical encoding algorithm efficiently handles over 9000 unique categorical values within the dataset. This robust solution ensures a meaningful representation of diverse categorical data.

- **Neural Network Architecture:** We utilize a state-of-the-art neural network architecture designed for mixed data types, allowing us to capture intricate patterns in the dataset. The model considers both categorical and numerical features, providing accurate predictions for flight departure delays.


## Dataset Description
The dataset employed in this study is comprehensive, spanning flight data from January 2018 to August 2023. It incorporates a diverse set of features, comprising detailed flight specifics, weather parameters, and geospatial information. With a total of 100,584,764 rows, the dataset's considerable size demands the application of sophisticated data processing methods and analytical approaches.

## Methodology

### Data Preparation

- **Handling Missing Values:** We address missing values in the dataset, excluding unsuitable columns and employing interpolation strategies where applicable. This meticulous data preparation ensures the reliability of subsequent analyses.

- **Standardization:** Numerical features are standardized to eliminate scale-related disparities, enabling fair and unbiased comparisons among features. This enhances the interpretability and performance of subsequent modeling and analytical procedures.

- **Categorical Encoding:** Our distinctive clustering-based categorical encoding algorithm efficiently manages over 9000 unique categorical values, ensuring a meaningful representation of diverse categorical data.

- **Outlier Removal:** Outliers, defined as values exceeding 3 standard deviations from the mean, are identified and removed to enhance model performance.

### Feature Selection

To mitigate multicollinearity, we strategically remove one feature from each correlated pair. Feature selection techniques, including correlation heatmaps and regression analysis, guide the identification of influential features.

### Exploratory Data Analysis

#### A. Effect of Airport Busyness on Departure Delays
- Investigated the relationship between airport busyness and departure delays, revealing a clear trend: as airports become busier, departure delays tend to increase.

#### B. Effect of Airlines Size on Departure Delays
- Explored the correlation between airline size and median departure delays, finding that larger airlines demonstrate lower delays, emphasizing the need for operational improvements in smaller carriers.

#### C. Correlation of Altitude with Delays
- Examined the impact of airport altitude on departure delays, concluding that no substantial correlation exists between altitude and delays.

### Geospatial Data Analysis

#### A. Hotspots of Flight Delays
- Visualized median flight delays across geographic locations, identifying hotspots, particularly on the East Coast, influenced by weather conditions.

#### B. Analysis of Delays by State
- Provided a comprehensive overview of average median delays across states, highlighting regional variations and informing strategic planning.

#### C. Proximity Analysis of Aviation Entities and Major Airports
- Studied the impact of aviation entities' proximity on departure delays at major airports, revealing a limited correlation, suggesting the presence of aviation facilities may not be a significant factor causing delays.


### Regression Analysis

- **Neural Network Architecture:** We employ a novel neural network architecture designed for mixed data types, featuring multiple input layers for categorical and numerical features. This architecture captures semantic relationships, enhancing the model's ability to learn complex patterns.

- **LightGBM Regression:** The LightGBM Regressor outperforms other regression models, leveraging its ability to handle complex relationships and non-linearities in the dataset.

### Classification Analysis

To facilitate classification, the target variable (DepDelay) is transformed into binary values. Various classification algorithms, including Random Forest, are employed to predict flight delays.

## Results

### Regression Model Performance

| Model                 | MAE (With OR) | RMSE (With OR) |
|-----------------------|---------------|----------------|
| Linear Regression     | 14.50         | 35.37          |
| Lasso Regression      | 14.75         | 35.63          |
| Ridge Regression      | 14.50         | 35.37          |
| ElasticNet Regression  | 14.80         | 35.66          |
| Neural Network        | 14.21         | 34.23          |
| LightGBM Regression   | 13.83         | 33.64          |

### Regression Model Performance with Outlier Removal and RFE

| Model                 | MAE           | RMSE           |
|-----------------------|---------------|-----------------|
| Linear Regression     | 13.94         | 34.26           |
| Lasso Regression      | 14.41         | 35.34           |
| Ridge Regression      | 13.94         | 34.26           |
| ElasticNet Regression  | 14.57         | 35.42           |
| LightGBM Regression   | 12.36         | 32.95           |

### Classification Results

| Algorithm               | F1 Score       | Accuracy       |
|-------------------------|----------------|-----------------|
| Gaussian Naive Bayes    | 0.10           | 0.67            |
| LightGBM Classifier     | 0.41           | 0.71            |
| Decision Tree           | 0.91           | 0.87            |
| Random Forest Classifier | 0.96           | 0.95            |

## Future Work

Our research opens avenues for future exploration and improvement in flight departure delay prediction. Key areas for further investigation include:

- **Refinement of Neural Network Architecture:** Explore advanced techniques, such as attention mechanisms, to capture more intricate patterns in the data.

- **Optimization of Categorical Encoding:** Extend and optimize the clustering-based categorical encoding algorithm to accommodate evolving datasets.

- **Impact of Specific Weather Conditions:** Conduct deeper exploration into the impact of specific weather conditions on departure delays, incorporating real-time data for more accurate predictions.

- **Integration of Advanced Models:** Explore advanced machine learning models and employ explainable AI techniques to enhance interpretability.

- **Collaboration with Aviation Stakeholders:** Collaborate with aviation stakeholders to implement and validate predictive models in real-world scenarios.

## Conclusion

In conclusion, our research provides valuable insights into key factors influencing flight departure delays in the United States. The project's innovative approaches, including a novel neural network architecture and clustering-based categorical encoding, contribute to a robust solution for predicting and understanding delays. Geospatial analysis and classification results further support targeted strategies for resource allocation, optimizing the economics of airlines, and improving passenger experiences.

## References

1. [U.S. Passenger Carrier Delay Costs - Airlines For America, May 2023](Reference Link 1)
2. [Cost of delay estimates 2019 - Federal Aviation Administration, Jul 2020](Reference Link 2)
3. [Cost of disrupted flights to the economy - AirHelp, Sep 2023](Reference Link 3)
4. Z. Guo, B. Yu, M. Hao, W. Wang, Y. Jiang, and F. Zong, "A novel hybrid method for flight departure delay prediction using random forest regression and maximal information coefficient," Aerospace Science and Technology, vol. 116, p. 106822, 2021
5. Q. Li, R. Jing, and Z. S. Dong, "Flight delay prediction with priority information of weather and non-weather features," IEEE Transactions on Intelligent Transportation Systems, 2023
6. J. G. M. Anguita and O. D. Olariaga, "Flight departure delay forecasting," Journal of Airport Management, vol. 17, no. 2, pp. 197–209, 2023
7. S. Mokhtarimousavi and A. Mehrabi, "Flight delay causality: Machine learning technique in conjunction with random parameter statistical analysis," International Journal of Transportation Science and Technology, vol. 12, no. 1, pp. 230–244, 2023
8. D. B. Bisandu PhD and I. Moulitsas PhD, "A deep bilstm machine learning method for flight delay prediction classification," Journal of Aviation/Aerospace Education & Research, vol. 32, no. 2, p. 4, 2023
9. A. Botchkarev, "Performance metrics (error measures) in machine learning regression, forecasting and prognostics: Properties and typology," arXiv preprint arXiv:1809.03006, 2018
10. ˇZ. Vujovi ́c et al., "Classification model evaluation metrics," International Journal of Advanced Computer Science and Applications, vol. 12, no. 6, pp. 599–606, 2021
11. N. Fei, Y. Gao, Z. Lu, and T. Xiang, "Z-score normalization, hubness, and few-shot learning," in Proceedings of the IEEE/CVF International Conference on Computer Vision, pp. 142–151, 2021
12. V. Barnett, T. Lewis, et al., *Outliers in statistical data*, vol. 3. Wiley New York, 1994


