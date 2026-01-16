# Anomaly-detection-with-autoencoder
This progect demonstates the application of an autoencoder neural network for monitoring user activity on a file repository. The goal is to detect unusual behavior that may indicate a security threat, thereby helping to prevent data breaches.

The model is trained to identify anomalies based on patterns in user activity logs. Anomalies could be complex and sophisticated, however, key markers of anomalous behaviour include:

- access from an uknown IP adress
- performing a new type of operations (e.g., a user who never deletes files suddenly does so)
- accessing files with unusual or atypical topics
- unusual activity during off-hours, such as evenings or weekends
- a critical number of 'access denied' errors in a short period
