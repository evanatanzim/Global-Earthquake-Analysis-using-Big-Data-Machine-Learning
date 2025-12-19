# Global-Earthquake-Analysis-using-Big-Data-Machine-Learning
A comprehensive big data analytics project analyzing 80,829 global earthquake records from 2015-2025 using Apache Spark distributed computing and Machine Learning. This project demonstrates end-to-end big data processing including architecture design, data exploration, transformation, and predictive modeling using PySpark MLlib.
# Global Earthquake Big Data & ML Analysis

A complete end‑to‑end big data and machine learning pipeline for global earthquake analytics using Apache Spark, PySpark MLlib, and interactive Plotly visualizations. The project processes ~80K+ events over 11 years to perform scalable preprocessing, feature engineering, exploratory analysis, clustering, and predictive modeling.

> Example repository name: `earthquake-big-data-analytics`

***

## Overview

This repository demonstrates how to use a modern big data stack to analyze a large, multi‑year global earthquake dataset. It covers:

- Distributed data ingestion and storage using Apache Spark  
- Schema inspection, statistical profiling, and data quality checks  
- Feature engineering for magnitude/depth categories and energy release  
- Interactive analytical dashboards with Plotly (HTML outputs)  
- Supervised learning (classification, regression) with PySpark MLlib  
- Unsupervised learning (geospatial clustering) and simple trend forecasting  

The workflow is designed to run seamlessly in Google Colab or any Spark‑enabled environment.

***

## Key Features

- **Scalable processing** of ~80K+ earthquake records with 20+ attributes  
- **Clean feature engineering**: time parsing, magnitude and depth bucketing, energy computation  
- **Rich visual analytics**: multi‑panel dashboards, geographic maps, and performance summaries  
- **Machine learning models**:
  - Random Forest classifier for magnitude category prediction  
  - Gradient boosting regressor for approximate magnitude estimation  
  - K‑means clustering for discovering seismic zones  
- **Trend analysis and forecasting** for future annual event counts  

---

## Repository Structure

```text
.
├─ notebooks/
│  └─ earthquake_big_data_colab.ipynb      # Main end‑to‑end notebook
├─ data/
│  └─ global_earthquakes_10yrs.csv         # Dataset (path reference; not committed)
├─ README.md                               # Project documentation
└─ LICENSE
```

> Adjust names/paths to match your actual repository layout.

---

## Getting Started

### Prerequisites

- Python 3.9+
- Java 8 (for Spark)
- Recommended: Google Colab or a local environment with sufficient memory

### Installation

```bash
# Clone this repository
git clone https://github.com/YOUR_USERNAME/earthquake-big-data-analytics.git
cd earthquake-big-data-analytics

# (Linux) Install Java 8 if needed
sudo apt-get update
sudo apt-get install -y openjdk-8-jdk-headless

# Install Python dependencies
pip install -r requirements.txt
```

### Dataset Setup

The project assumes a CSV file similar to:

- File: `global_earthquakes_10yrs.csv`  
- Columns include:
  - `time`, `latitude`, `longitude`, `depth`, `mag`
  - event metadata (place, id, network, etc.)

Place the file in:

```text
data/global_earthquakes_10yrs.csv
```

or update the notebook path accordingly.

***

## Running the Notebook

### Option 1: Google Colab

1. Upload the notebook in `notebooks/` to Colab.  
2. Mount Google Drive and place the dataset in your Drive path (update the path in the notebook accordingly).  
3. Run all cells from top to bottom:
   - Environment and Spark initialization  
   - Data loading and repartitioning  
   - Transformations and feature engineering  
   - Visualizations and dashboards (HTML exports)  
   - Model training, evaluation, clustering, and forecasting  

### Option 2: Local Jupyter

```bash
jupyter notebook notebooks/earthquake_big_data_colab.ipynb
```

Ensure Spark and Java environment variables are correctly configured before running.

***

## Technical Stack

| Component          | Technology      |
|-------------------|-----------------|
| Language          | Python          |
| Distributed Engine| Apache Spark    |
| ML Library        | PySpark MLlib   |
| Visualization     | Plotly + Kaleido|
| Data Handling     | PySpark, pandas |
| Forecasting       | scikit‑learn    |

***

## Highlights

- Efficient handling of tens of thousands of seismic events using Spark’s DataFrame API  
- Clean separation of raw ingestion, derived features, and saved, partitioned outputs  
- Consistent use of HTML dashboards for interactive exploration and reporting  
- Reusable patterns for:
  - Assembling feature vectors  
  - Training and evaluating ML models at scale  
  - Visualizing geospatial clusters and model performance  

***

## How to Cite / Use

If you build on this work in academic or industry settings, consider referencing the repository URL and acknowledging the Spark‑based big data and ML workflow.

***

## Contributing

Contributions and improvements are welcome:

1. Fork the repository  
2. Create a feature branch: `git checkout -b feature/your-feature-name`  
3. Commit your changes: `git commit -m "Add your feature"`  
4. Push the branch: `git push origin feature/your-feature-name`  
5. Open a pull request describing your changes  

***

## License

This project is released under the MIT License. See `LICENSE` for details.
