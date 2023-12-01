# <span style="font-size: 32px;">**OBESITY RISK PREDICTION**</span>

## Business Understanding

Obesity and overweight can be defined as abnormal or excessive fat build-up that poses a risk to health. Obesity often results from taking in more calories than are burned by exercise and normal daily activities. Obesity occurs when a person's body mass index is 30 or greater. Body mass index (BMI) is a measure of body fat based on height and weight. The rising rate of obesity in the medical field poses significant challenges to both patients and healthcare providers. Addressing obesity at an early stage is important for preventive healthcare and overall well-being. Our business centers around leveraging advanced machine learning techniques to predict the risk of obesity, providing valuable insights for healthcare providers to proactively intervene and offer personalized care.

The key stakeholders are healthcare providers. They include physicians, nurses, dietitians, and other healthcare professionals who are involved in patient care. Patients also benefit from personalized healthcare interventions based on their obesity risk. Healthcare systems are responsible for implementing and integrating the predictive model into existing healthcare frameworks.

## Problem Statement

Overweight and obesity are major risk factors for a number of chronic diseases, including cardiovascular diseases such as heart disease and stroke, which are the leading causes of death worldwide. Rates of overweight and obesity continue to grow in adults and children. Once considered a problem only in high-income countries, overweight and obesity are now dramatically on the rise in low- and middle-income countries, particularly in urban areas. Obesity in childhood is associated with a wide range of serious health complications and an increased risk of premature onset of related illnesses. Without intervention, children and adolescents with obesity will likely continue to be obese into adulthood. The goal is to develop a robust and accurate obesity risk prediction model. This model aims to evaluate an individual's likelihood of being classified as at-risk for obesity based on a set of pertinent features. This will enhance the ability to identify individuals at risk of obesity early on, allowing for proactive intervention and personalized health plans.

## Objectives

- To explore the relationship between obesity and key features such as weight, height, age and gender. Determine if these features contribute to the likelihood of obesity.
- To develop a machine learning model capable of predicting obesity risk based on individual characteristics as input variables.
- To optimize the predictive accuracy of the model, ensuring reliable and actionable results for healthcare providers. Ensure the model provides interpretable insights, allowing healthcare professionals to understand and trust the predictions.

## Data Understanding

The data consists of the estimation of obesity levels in people from the countries of Mexico, Peru and Colombia, with ages between 14 and 61 and diverse eating habits and physical conditions. It can be found in the file ObesityDataSet.csv.

## Exploratory Data Analysis

We perform analysis to extract insights, identify patterns and draw conclusions from the data.

We compare the relationship between the numeric variables using a correlation matrix.

![Correlation Matrix](images/Correlation%20Matrix.png)

We also visualize the obesity types.

![Obesity Types](images/Distribution%20of%20Obesity%20Types.png)

## Modeling
1. **Data Preprocessing.** Prepare the data for modeling by addressing the data types for the categorical columns.

2. **Perform a Train-Test Split.** For a complete end-to-end ML process, we need to create a holdout set that we will use at the very end to evaluate our final model's performance.

3. **Build and Evaluate a Simple Baseline Model.** Without performing any preprocessing or hyperparameter tuning, build and evaluate a vanilla logistic regression model.

4. **Build and Evaluate Additional Models.** Create versions of the simple model with tuned hyperparameters. Build a more complex model, Random Forest and compare the selected metric with that of the simple models.

5. **Choose and Evaluate a Final Model.** Preprocess the full training set and test set appropriately, then evaluate the final model with various classification metrics.
   
We visualize the performance of all our logistic regression models using a bar graph.

![Precision for Regression](images/Comparison%20of%20Precision%20Scores.png)

## Evaluation

Based on the metrics for our final model, it demonstrates strong performance in terms of precision, accuracy, recall, and F1 score on both the training and test sets. The precision on the training set is notably high at 0.921, indicating that the model is effective in minimizing false positives, which is crucial in the context of predicting the risk of someone being obese. This is particularly important for healthcare providers as it ensures that when the model predicts a positive outcome (risk of obesity), it is highly reliable.

In healthcare, high precision is crucial to avoid false alarms, ensuring that when the model predicts a positive outcome, the healthcare providers can trust the result. The strong performance on the test set suggests that the model generalizes well to unseen data, making it a reliable tool for healthcare providers in assessing obesity risk.

## Conclusion

The final model, a Random Forest Classifier, has demonstrated great performance in predicting the risk of obesity. With high precision, accuracy, recall, and F1 score on both the training and test sets, the model showcases its effectiveness in identifying individuals at risk. This precision is particularly crucial in healthcare, where minimizing false positives is essential to ensure reliable predictions.

## Recommendations

-**Intergrate model into workflow.** Based on the model's success, it is recommended to integrate it into the healthcare provider's workflow for assessing obesity risk. Healthcare professionals can use the model as an additional tool to identify individuals who may benefit from preventive interventions or closer monitoring.

-**Collaboration between data scientists and healthcare providers** is recommended to fine-tune the model based on real-world feedback and evolving healthcare practices. Considering the specific requirements and constraints of the healthcare setting, potential adjustments may be made based on the stakeholders' feedback.

## Next Steps

-**Continuous Monitoring and Improvement:** Regularly monitor the model's performance in a real-world healthcare setting. Collect feedback from healthcare providers to identify any challenges or areas for improvement.

-**Extended Stakeholder Involvement:** Involve a broader range of stakeholders, including patients, in the model development process to incorporate diverse perspectives and address ethical considerations.

-**Model Updates:** Periodically retrain the model with new data to ensure its relevance and effectiveness over time. Stay informed about advancements in obesity research to incorporate the latest findings into the model.
