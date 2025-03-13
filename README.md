# Forecasting-Volcanic-Eruption-ML
Forecasting Volcanic Eruption and Impact Assessment

**Problem Statement:** 
The problem at hand entails analyzing a sequence of sensor readings taken at consecutive time steps to address two distinct tasks related to volcanic eruptions. Firstly, the aim is to devise an effective approach that accurately estimates the remaining time units until eruption for a given observation. This observation can have sensor readings of varying lengths. By leveraging the information within the sensor data, the objective is to provide timely predictions for the impending eruption, enabling proactive measures to be taken to ensure the safety of affected areas and populations.
The second task involves estimating the magnitude of the impending volcanic eruption. Utilizing the provided observation, the goal is to develop a methodology that can estimate the severity and intensity of the eruption event. Despite the absence of the eruption magnitude in the observations, it is possible to estimate the tilt erupt value, which represents the last sensor reading corresponding to the moment of eruption. This particular value exhibits a strong correlation with the magnitude of the eruption. By estimating the tilt erupt value, we can obtain a reliable estimation of the eruption's impact. The obtained estimation is crucial for emergency management and response planning, allowing authorities to allocate appropriate resources and implement necessary measures to mitigate the potential impacts of the volcanic eruption on surrounding areas.

**Solution:**
We set the number of subsequences from each file to 1, with a subsequence length of 5, resulting in a total of 189*5 observations (945 in total). This configuration aims to maintain the number of observations within the range of 900 to 1600, ensuring the extraction of meaningful features and mitigating the risk of underfitting. I established a dataframe to store the observation number, time to eruption, and pressure at the time of eruption. Additionally, I created a second dataframe to capture the shortest time to erupt among the subsequences of 5 values. I then computed statistics including the minimum, maximum, median, average, and standard deviation on this dataframe of the most recent time to erupt. Furthermore, I visualized the least recent time to erupt dataframe using line plots and histograms. Tried to utilize TSFresh to extract features from the data but it did not work as expected, and employed LazyPredict to predict the time taken by different models.

**Procedure:**

1.**Data Preparation**: Preprocess the raw dataset to generate labeled samples. Split the generated samples into training and testing subsets. Consider any necessary feature engineering techniques to enhance the predictive power of the data.

2.**Regression Technique Selection**: Identify and select suitable regression techniques to be evaluated for their effectiveness in anticipating and comprehending volcanic phenomena. This may include popular methods such as linear regression, decision trees, random forests, support vector regression, boosting algorithms, or neural networks.

3.**Model Training**: Train the selected regression models on the training subset of the dataset. Adjust hyperparameters and perform model optimization techniques, such as cross-validation, to ensure optimal performance. During the process of cross-validation, it is advisable to ensure an unbiased estimate of performance measures by considering different volcanoes in both the train and test sets. This approach helps to mitigate any potential biases that may arise from overfitting to specific volcano data, allowing for a more robust evaluation of the regression model's performance.

4.**Model Evaluation**: Evaluate the trained regression models using the testing subset of the dataset. Measure their performance using appropriate evaluation metrics such as mean squared error, root mean squared error, or R-squared value.

5.**Results Analysis**: Analyze the performance of the regression models and compare their effectiveness in anticipating and comprehending volcanic phenomena. Identify the most suitable techniques that yield the best predictive capabilities.

6.**Model Refinement**: Fine-tune the selected regression model(s) based on the analysis of the results. This may involve adjusting hyperparameters, incorporating feature selection methods, or exploring ensemble techniques to further enhance performance.

7.**Final Evaluation**: Validate the refined regression model(s) on unseen data or real-world observations, if available. Assess the model's ability to anticipate and comprehend volcanic phenomena accurately.

8.**Discussion and Conclusion**: Summarize the findings, limitations, and implications of the study. Discuss the potential applications of the regression model(s) in enhancing the understanding and prediction of volcanic activities.

9.**Further Research**: Identify any areas for improvement or additional research that could enhance the accuracy and effectiveness of regression techniques in anticipating and comprehending volcanic phenomena. 

