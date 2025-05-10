# Iris Flower Classification Project

This project implements a machine learning pipeline for classifying Iris flowers using the famous Iris dataset. The project includes data processing, outlier detection, and model training components.

## Project Structure

```
├── artifacts/
│   ├── raw/            # Raw data files
│   ├── processed/      # Processed data files
│   └── models/         # Trained models and evaluation metrics
├── src/
│   ├── data_processing.py    # Data processing and outlier handling
│   ├── model_training.py     # Model training and evaluation
│   ├── logger.py            # Logging configuration
│   └── custom_exception.py   # Custom exception handling
├── pipeline/
│   └── training_pipeline.py  # Main training pipeline
└── README.md
```

## Features

- Data processing and cleaning
- Outlier detection and handling using IQR method
- Model training using Decision Tree Classifier
- Model evaluation with multiple metrics
- Logging system for tracking operations
- Custom exception handling

## Prerequisites

- Python 3.x
- Required Python packages:
  - pandas
  - numpy
  - scikit-learn
  - seaborn
  - matplotlib
  - joblib

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-name>
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Place your raw data file in the `artifacts/raw` directory.

2. Run the training pipeline:
```bash
python pipeline/training_pipeline.py
```

## Data Processing

The data processing pipeline includes:
- Loading the Iris dataset
- Handling outliers using IQR method
- Splitting data into training and testing sets

## Model Training

The model training process includes:
- Training a Decision Tree Classifier
- Model evaluation using:
  - Accuracy Score
  - Precision Score
  - Recall Score
  - F1 Score
  - Confusion Matrix

## Outlier Detection

The project implements outlier detection using the IQR (Interquartile Range) method:
- Calculates Q1 (25th percentile) and Q3 (75th percentile)
- Computes IQR = Q3 - Q1
- Identifies outliers as values below (Q1 - 1.5*IQR) or above (Q3 + 1.5*IQR)
- Replaces outliers with the median value

## Logging

The project includes a comprehensive logging system that tracks:
- Data loading operations
- Outlier detection and handling
- Model training progress
- Model evaluation metrics

## Error Handling

Custom exception handling is implemented throughout the pipeline to ensure robust operation and meaningful error messages.

## Output

The pipeline generates:
- Processed data files in `artifacts/processed/`
- Trained model in `artifacts/models/`
- Confusion matrix visualization
- Log files with operation details

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Iris dataset from UCI Machine Learning Repository
- Scikit-learn library for machine learning tools
- Pandas and NumPy for data manipulation 