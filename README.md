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


    
