# Stroke Prediction
**Context**
  - According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.
  
**Source of data**
  - Source : https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

**Brief description of data**
  - This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient.

  - Target column is stroke. Predicting whether patient will suffer from a stroke or not.

**Attribute Information**
  1. id: unique identifier
  2. gender: "Male", "Female" or "Other"
  3. age: age of the patient
  4. hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
  5. heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
  6. ever_married: "No" or "Yes"
  7. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
  8. Residence_type: "Rural" or "Urban"
  9. avg_glucose_level: average glucose level in blood
  10. bmi: body mass index
  11. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
  12. stroke: 1 if the patient had a stroke or 0 if not
    *Note: "Unknown" in smoking_status means that the information is unavailable for this patient

**Key Findings**
  - The dataset comprises data gathered from a substantial sample size of 5,110 patients, encompassing the 11 factors highlighted in the previous slide.
  - Notably, the dataset exhibits a significant class imbalance, with 249 patients experiencing a stroke, while 4,861 patients did not encounter a stroke.
  - Age analysis reveals a predominant occurrence of strokes among individuals aged 60 years and older.
  - An intriguing finding is that patients employed in private sectors display a higher susceptibility to stroke.
  - Surprisingly, non-smoking patients present a higher risk of suffering from a stroke, although it is essential to emphasize that this observation does not endorse or encourage smoking in any way.

**Model Evaluation**

Since the predictions are for a stroke dataset, it is crucial to prioritize recall  in order to correctly identify stroke cases. Accuracy is still important, but it's crucial to minimize false negatives (misclassifying stroke cases as non-strokes).
      - Recall: Recall is a measure of how well our model can catch all the people who actually had strokes from the entire group of people who had strokes. In other words, it tells us how good the model is at identifying the actual stroke cases correctly.
      -Accuracy: Accuracy is a measure of how well our model can correctly predict both stroke and non-stroke cases overall. It considers both the correct predictions and the mistakes.

  - Among these options, the model with the highest recall is AdaBoost-Tuned, achieving a recall of 97%. Although its accuracy is relatively low at 45%, it is important to note that prioritizing recall aims to capture as many stroke cases as possible, reducing the risk of false negatives.
  - However, if you prefer a better balance between accuracy and recall, the GradientBoosting model may be a good choice, as it has an accuracy of 92% and a recall of 23%.
Ultimately, the best model choice depends on the specific requirements and priorities of the stroke dataset analysis. Consider the trade-off between recall and accuracy and choose the model that aligns best with your needs.

**Suggestions for further improving the Stroke Prediction Model**
- SMOTE (Synthetic Minority Over-sampling Technique): Since the dataset likely has an imbalance between stroke and non-stroke cases, SMOTE can be employed to generate synthetic samples of the minority class (in this case, stroke cases) to balance the class distribution. This technique can help prevent bias towards the majority class and improve the model's ability to recognize stroke cases.
- PCA(Principal Component Analysis) is a dimensionality reduction technique that can be utilized to reduce the number of features in the dataset while preserving most of the important information. By applying PCA, you can simplify the model and potentially enhance its performance by focusing on the most informative features.
- Implementing neural networks, particularly deep learning architectures, can be beneficial for complex and high-dimensional datasets like stroke prediction. Neural networks can automatically learn intricate patterns and relationships in the data, leading to potentially improved accuracy and recall.
- As I've mentioned, improving the class balance by collecting more data, especially stroke cases, can be highly beneficial. A larger and more balanced dataset allows the model to learn better from representative examples of both classes, which can result in a more robust and accurate model.
