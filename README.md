This project aims to automate the process of identifying and managing forensic evidence by using image classification and risk prediction models. The system leverages a Convolutional Neural Network (CNN) to classify the type of evidence (e.g., fingerprint, gun, stained cloth) based on the image uploaded by the user. Once the evidence type is predicted, environmental variables (such as temperature, humidity, vibration, etc.) are autofilled with default values optimized for that type of evidence. Additionally, the system predicts whether the evidence is at high risk or low risk of deterioration using an ensemble machine learning model. After the initial prediction, the project integrates a real-time IoT simulation to continuously change the environmental variables, updating the risk status dynamically. If any environmental changes threaten the integrity of the evidence, real-time alerts are issued to notify the user to take corrective action, helping to ensure that the evidence remains in usable condition throughout the investigation.

In forensic science, it is crucial to ensure the integrity of evidence to guarantee its usability during legal proceedings. Various types of evidence (e.g., fingerprints, firearms, or stained cloth) are highly sensitive to environmental conditions like temperature, humidity, and vibration. If these environmental conditions are not monitored and controlled, the evidence can deteriorate or become contaminated, rendering it useless in an investigation. Traditionally, environmental monitoring is a manual process, prone to human error. Furthermore, determining the appropriate storage conditions and identifying high-risk evidence early can be challenging.

This project addresses these challenges by:
1.	Automatically predicting the type of evidence based on uploaded images using CNNs.
2.	Predicting the risk status (high risk or low risk) of the evidence using environmental data.
3.	Monitoring environmental conditions in real-time through simulated IoT data to track any changes that could affect the evidence.
4.	Issuing real-time alerts if the risk status of the evidence changes, allowing for quick intervention to maintain integrity.

MODELS EXPLANATION AND JUSTIFICATION:
1. Convolutional Neural Network (CNN) – For Evidence Type Classification
A Convolutional Neural Network (CNN) is a deep learning architecture specifically designed for image classification tasks. CNNs are chosen for this project because they excel at identifying patterns and features in image data, such as textures, edges, and shapes. This makes them well-suited for differentiating between various types of forensic evidence, such as fingerprints, guns, and stained cloth.
•	Justification: CNNs provide high accuracy for image classification tasks and can generalize well to unseen data when trained properly. They are ideal for this project, where the type of evidence needs to be identified based on uploaded images.

2. Ensemble Model – For Risk Prediction (High/Low Risk)
The project uses an ensemble of machine learning models (Random Forest, XGBoost, and Gradient Boosting) to predict whether the evidence is at high risk or low risk based on environmental variables (e.g., temperature, humidity). Ensemble models combine the predictions of multiple algorithms to improve accuracy and reduce the likelihood of overfitting.
•	Justification: Ensemble models are highly effective for tabular data and can handle small datasets better by leveraging the strengths of individual algorithms. This approach ensures more reliable predictions for risk assessment.
