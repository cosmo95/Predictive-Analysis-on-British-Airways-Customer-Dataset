# British Airways Customer Booking Prediction Analysis

## Project Overview
This project focuses on analyzing customer booking data from British Airways to predict whether a customer will complete a booking or not. The goal is to identify key factors influencing booking completion and to build a machine learning model to assist in targeted marketing or operational strategies.

## Data Source
The analysis is based on the `customer_booking.csv` dataset, which contains various features related to customer travel preferences and booking behavior.

## Analysis Highlights & Model Performance

### Key Findings:
*   **Class Imbalance**: The dataset exhibits a significant class imbalance, with approximately 85% of bookings not completed and 15% completed.
*   **Top Features**: The most influential factors in predicting booking completion include `purchase_lead` (how far in advance a booking is made), `flight_hour`, `length_of_stay`, `num_passengers`, and `flight_duration`.

### Model Performance (Random Forest Classifier):
Using Stratified K-Fold Cross-Validation, the Random Forest model achieved:
*   **Average Accuracy**: ~85.15%
*   **Average Precision (for 'Booking Complete' class)**: ~51.46%
*   **Average Recall (for 'Booking Complete' class)**: ~12.62%
*   **Average F1-Score (for 'Booking Complete' class)**: ~20.27%

The model shows high overall accuracy primarily due to its strong performance on the majority class (non-completed bookings). However, its ability to correctly identify actual completed bookings (the minority class) is limited, as indicated by the low recall and F1-score for this class. Further efforts would be needed to improve the detection of completed bookings, potentially through techniques addressing class imbalance or alternative modeling approaches.

## Repository Contents
*   `British_Airways_Customer_Booking_Prediction_Analysis.ipynb`: The Jupyter/Colab notebook containing the full analysis, including data loading, EDA, model training, evaluation, and visualization.
*   `README.md`: This file, providing an overview of the project.
*   `.gitignore`: Specifies files and directories to be ignored by Git.

## How to Run the Notebook
1.  Open the `British_Airways_Customer_Booking_Prediction_Analysis.ipynb` file in Google Colab.
2.  Ensure `customer_booking.csv` is available in your Colab environment (e.g., uploaded or mounted from Google Drive).
3.  Run all cells sequentially to reproduce the analysis and model results.
