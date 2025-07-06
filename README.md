# Detecting Anomalies in Ethereum Transactions using ML

This project uses **machine learning** to find unusual or suspicious transactions on the **Ethereum blockchain**.

It’s a project that helps understand:
- How real Ethereum transactions work
- How to clean and explore data
- How to detect anomalies using ML and deep learning

---

## What Is Ethereum?

Ethereum is a popular cryptocurrency like Bitcoin. People send ETH (Ether) using the blockchain. These transactions are **public** and can be analyzed to detect suspicious behavior, like:
- Unusually high fees
- Very small or very large ETH transfers
- Strange patterns

---

## Project Goal

The main goal of this project is to:
**Detect abnormal transactions** using ML models by analyzing ETH amount, fee paid, and timing.

---

## Dataset Description

The original Ethereum transaction dataset used in this project is available on Kaggle:
🔗 https://www.kaggle.com/datasets/ikjotsingh221/ethereum-transaction-dataset-raw/data

Each row in the dataset is one Ethereum transaction.

| Column | Description |
|--------|-------------|
| `Blockno` | The block number containing the transaction |
| `UnixTimestamp` | Timestamp in Unix format |
| `DateTime (UTC)` | Human-readable date and time |
| `Value_IN(ETH)` | ETH received in the transaction |
| `Value_OUT(ETH)` | ETH sent out (if applicable) |
| `CurrentValue @ $3083...` | Estimated USD value of ETH at the time (fixed rate) |
| `TxnFee(ETH)` | Gas/fee paid for the transaction in ETH |
| `TxnFee(USD)` | Fee converted to USD |
| `Historical $Price/Eth` | ETH to USD price at the time of transaction |

---

## Tools & Libraries

This project uses:
- **Python**
- **Jupyter Notebook**
- `pandas`, `numpy`, `matplotlib`, `seaborn` – for data handling and plotting
- `scikit-learn` – for machine learning models
- `PyTorch` – for the deep learning autoencoder

---

## Notebooks Summary

| Notebook | What It Does |
|----------|----------------|
| `01_data_preprocessing` | Clean data and create new features |
| `02_eda_visualization` | Explore data using plots |
| `03_anomaly_detection` | Use ML models to find anomalies |
| `04_autoencoder_anomaly` | Use deep learning to detect anomalies |

---

## Models Used

### * Isolation Forest
Detects unusual data points in the dataset.

### * One-Class SVM
Tries to learn the boundary of normal transactions.

### * Autoencoder (Deep Learning)
Learns to recreate normal behavior and flags anything it can't recreate well.

---

## Sample Visualizations

### * ETH Value vs Txn Fee
* [Value vs Fee](images/eth_value_vs_fee.png)

### * Isolation Forest Anomalies
* [IF Anomalies](images/isolation_forest_anomalies.png)

### * Autoencoder Anomalies
* [Autoencoder](images/autoencoder_anomalies.png)

### * Distribution of Txn Fees
* [Fee Histogram](images/txn_fee_distribution.png)





