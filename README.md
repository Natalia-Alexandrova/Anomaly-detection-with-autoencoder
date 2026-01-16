# Anomaly-detection-with-autoencoder
This progect demonstates the application of an autoencoder neural network for monitoring user activity on a file repository. The goal is to detect unusual behavior that may indicate a security threat, thereby helping to prevent data breaches.

The model is trained to identify anomalies based on patterns in user activity logs. Anomalies could be complex and sophisticated, however, key markers of anomalous behaviour include:

- access from an uknown IP adress
- performing a new type of operations (e.g., a user who never deletes files suddenly does so)
- accessing files with unusual or atypical topics
- unusual activity during off-hours, such as evenings or weekends
- a critical number of 'access denied' errors in a short period

## The key results
- This project has established a machine learning pipeline for the detection of suspicious user activity on a file repository.
- EDA pinpointed unknown IPs, new file operation types and filenames dissimilarity as primary anomaly indicators.
- User activity was transformed into a temporal sequence tensor, with shape = (3,15), encoding the categorical features for model consumption.
- An autoencoder neural network with a bottleneck (16-8-4-8-16) was developed. The use of Batch Normalization and LeakyReLU activations ensured stable and efficient training. The model's hyperparameters were tuned using an Optuna study.
- The model's anomaly detection mechanism, based on reconstruction error, proved accurate. On the test day, the model achieved a precision of 1 (no false positives) and a recall of 1, indicating it caught all true anomalies (events from unknown IP and new operation-type).
- The analysis of detected anomalies provides actionable intelligence, showing a peak in suspicious activity during the evening hours (5-6 PM), involving interaction with atypical documents.
