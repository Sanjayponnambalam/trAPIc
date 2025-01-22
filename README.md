# trAPIc
trAPIc is a Machine Learning project designed to analyze traffic patterns and detect anomalies within a web server's log data. It leverages unsupervised learning techniques to gain valuable insights into server traffic and potential security threats.

---

## Project Overview
### Anomaly Detection
- Detects anomalies in request frequency, such as DDoS attacks and suspicious activities.
- Employs Autoencoders algorithm for Anomaly detection.

---

## Dataset

The dataset includes the following columns:
- `IP`
- `Timestamp`
- `Method`
- `Endpoint`
- `StatusCode`
- `ResponseSize`
- `Referrer`
- `UserAgent`

---

## Installation

### Prerequisites
- Python 3.x
- Jupyter Notebook

### Setup Instructions

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/trAPIc.git
    cd trAPIc
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```
---

## Principal Component Analysis

![PCA Plot](https://github.com/Sanjayponnambalam/trAPIc/blob/main/img/PCA.png)

### Insights

- The plot suggests that the data exhibits a relatively consistent pattern in the PCA space. This might indicate that the traffic patterns are generally predictable and follow a regular schedule.
- To confirm or identify potential anomalies, it would be necessary to apply anomaly detection algorithms to the data and examine the results. 
- Here, we use Autoencoders to identify subtle deviations that might not be visually apparent in the PCA plot.

---
## Train Loss vs Validation Loss

![Train vs Validation Loss](https://github.com/Sanjayponnambalam/trAPIc/blob/main/img/TV%20Loss.png)

### Insights

- The training and validation loss curves are closely aligned throughout the training process, suggesting that the model generalizes well to unseen data and is not overfitting.
- After around 20 epochs, the training and validation losses start to stabilize and converge, indicating that the model is no longer learning significantly from additional epochs.
- The final values of both losses are low and plateaued, indicating that the model has achieved a stable state and has effectively minimized reconstruction error.

---

## Model Training and Evaluation

- `Mean Reconstruction Error: 0.342398156416376`
- `Standard Deviation of Reconstruction Error: 0.19965641892163488` 
- `Threshold for Anomalies: 0.9413674131812806`


### Insights

- A value of 0.342 indicates that the model has a relatively low average error when reconstructing the normal data patterns. This suggests the model has learned the underlying structure of the dataset effectively.
- The standard deviation of 0.200 shows that the reconstruction errors are consistent and not highly variable, indicating a stable model performance.
- The threshold of 0.941 implies that any data point with a reconstruction error above this value will be classified as an anomaly. This threshold balances between sensitivity and specificity for detecting anomalies.
  
---

## Reconstruction Error Distribution

![Reconstruction Error Distribution](https://github.com/Sanjayponnambalam/trAPIc/blob/main/img/Error%20Distribution.png)

### Insights

- **Total Test Samples:** 3600
- **Number of Anomalies Detected:** 16



    
