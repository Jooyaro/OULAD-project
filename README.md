# OULAD-project
The goal of this project is to predict the students’ success and failure in online courses and identify those who are at risk of failure or withdrawal, using the anonymized Open University Learning Analytics Dataset (OULAD, https://analyse.kmi.open.ac.uk/open_dataset).

For this project, we collected the partial behavioral data of students from the $1/3$ and $1/2$ periods of courses and predicted their likelihood of completing the courses using various machine learning models. The original datasets consist of seven datasets used in this project, containing information about courses, students, and their interactions with the virtual learning environment (VLE) across seven selected courses (modules). Specifically, the datasets include demographic information about students (gender, age, IMD, region, highest education, disability), behavioral data (number of clicks and views by material), and assessment data (homework submission dates, scores). 


### Supervised Learning Models and Results
Six supervised learning algorithms were used to predict the success or failure of students based on their data from the $1/3$ and $1/2$ periods of the courses: Logistic Regression with Lasso Regularization, Support Vector Machine (SVM), Decision Tree, Random Forest, Naïve Bayes, and Bayesian Neural Network. Among them, we would like to describe three algorithms in more detail: Random Forests, Naïve Bayes Classifier, and Bayesian Neural Network.

The following tables present the accuracy and F1 score of six supervised learning models for the $1/3$ period data and $1/2$ period data. The F1 score, reflecting the model's overall performance, is the harmonic average of precision and recall. Among these models, Random Forests demonstrated superior performance.

| Model                        | Accuracy | F1 Score |
|------------------------------|----------|----------|
| Logistic Regression (Lasso)  | 0.743    | 0.752    |
| Support Vector Machine       | 0.674    | 0.741    |
| Decision Tree                | 0.740    | 0.748    |
| Random Forests               | 0.754    | 0.761    |
| Naive Bayes Classifier       | 0.707    | 0.721    |
| Bayesian Neural Network      | 0.659    | 0.709    |


| Model                        | Accuracy | F1 Score |
|------------------------------|----------|----------|
| Logistic Regression (Lasso)  | 0.783    | 0.790    |
| Support Vector Machine       | 0.716    | 0.769    |
| Decision Tree                | 0.771    | 0.779    |
| Random Forests               | 0.790    | 0.795    |
| Naive Bayes Classifier       | 0.745    | 0.759    |
| Bayesian Neural Network      | 0.701    | 0.763    |


Notably, the most influential feature across these intervals is the average assessment score. This finding suggests that higher assessment scores are reliable indicators of a student's likelihood to pass or fail the module by the final period. Additionally, the timing of assignment submissions emerges as another significant predictor; submissions made earlier than the deadline are associated with a higher probability of passing the module.

Adding to this, it's interesting to note how these features align with educational psychology theories, emphasizing the importance of timely feedback and the positive effects of continuous assessment on student performance. Moreover, engagement metrics, such as the number of attempts at the learning platform, still contribute valuable insights into student success rates. This underscores the multifaceted nature of learning analytics and the potential of machine learning models to synthesize complex data into actionable predictions.

