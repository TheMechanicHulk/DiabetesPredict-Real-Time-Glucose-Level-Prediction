# DiabetesPredict: Real-Time Blood Glucose Level Prediction System

## Overview
DiabetesPredict is a prototype system designed for real-time blood glucose level prediction in Type-1 diabetic patients. The system is built around an LSTM-RNN model that predicts glucose levels based on past readings and insulin intake. It is designed to run on low-power microcontrollers, such as the **Raspberry Pi Zero**, offering a cost-effective, portable solution for continuous glucose monitoring and diabetes management.

The system includes an OLED **RPI LCD 1.44 JOY Display** to visualize the predicted glucose levels and provide corrective actions based on the patient's real-time sensor data.

## Features
- **LSTM-RNN Model**: Designed to predict blood glucose levels using past glucose readings, insulin dosage, and other relevant data.
- **Real-Time Monitoring**: Deployed on **Raspberry Pi Zero**, enabling real-time glucose prediction with minimal computational resources.
- **User-Friendly Interface**: Provides a simple OLED display for real-time feedback on glucose levels and suggested corrective actions.
- **Cost-Effective Solution**: Uses affordable components, making it accessible for personal and healthcare use.
- **Sensor Integration**: Captures real patient data from a wearable glucose sensor for accurate predictions.

## Workflow
1. **Data Collection**:
    - Collected real-time glucose readings from a Type-1 diabetes patient using a continuous glucose monitor (CGM) sensor.
    - Utilized past readings, insulin dosages, and meal timings to feed the LSTM-RNN model.
    
2. **Model Development**:
    - Developed an **LSTM-RNN** model using **Keras** to predict future glucose levels based on the history of glucose readings.
    - The model was trained on real patient data, ensuring the system's reliability for personalized diabetes management.
    
3. **Raspberry Pi Integration**:
    - Deployed the trained model on **Raspberry Pi Zero** for real-time predictions.
    - Integrated an **OLED RPI LCD 1.44 JOY Display** for user-friendly feedback on glucose levels and suggested actions.

4. **System Architecture**:
    - The system continuously receives sensor data (e.g., glucose levels) and makes predictions every 5 minutes.
    - Display updates with the predicted glucose value and any suggested corrective action (e.g., insulin dosage or carbohydrate intake).
    
## Hardware & Tools
- **Raspberry Pi Zero**: The main processing unit for running the prediction model.
- **RPI LCD 1.44 JOY Display**: OLED screen for visualizing glucose predictions.
- **CGM Sensor**: Continuous Glucose Monitor for collecting real-time glucose data.
- **Python & Keras**: For developing the LSTM-RNN model.
- **NumPy & Pandas**: Data processing and manipulation libraries.

## Installation and Setup
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/TheMechanicHulk/DiabetesPredict-Real-Time-Glucose-Level-Prediction.git
    cd DiabetesPredict-Real-Time-Glucose-Level-Prediction
    ```

2. **Install Dependencies**:
    - Install necessary Python libraries on the Raspberry Pi:
    ```bash
    pip install numpy pandas keras tensorflow matplotlib
    ```

3. **Run the System**:
    - Ensure the Raspberry Pi Zero is connected to the glucose sensor.
    - Start the real-time prediction system:
    ```bash
    python diabetes_predict.py
    ```
    - The display will show the current glucose level and predicted value along with corrective actions if needed.

## Model Performance
- **Training Data**: The model was trained using real-world data from a Type-1 diabetic patient, consisting of over 10,000 glucose readings.
- **Model Accuracy**: The LSTM-RNN model achieved an **accuracy of 85%** in predicting glucose levels, offering reliable short-term forecasts.
- **Real-Time Efficiency**: The system performs predictions in less than 2 seconds, ensuring real-time operation on resource-constrained hardware.

## Results
- The system successfully predicts glucose levels with high accuracy in real-time, providing timely feedback to the patient.
- The use of a low-cost microcontroller and display makes the solution highly accessible.
- Suggested corrective actions are displayed based on the predicted glucose level and current insulin intake.

## Future Improvements
- **Enhanced Prediction Accuracy**: Further training with a larger dataset could improve the model's accuracy.
- **Integration with Mobile App**: Adding Bluetooth or Wi-Fi functionality to communicate with a mobile app for remote monitoring.
- **Advanced Display Features**: Incorporate a graphical user interface (GUI) to show glucose trends over time and offer more detailed insights.

## File Structure
```bash
├── data/              # Contains training data (real glucose sensor data)
├── models/            # Saved LSTM-RNN model
├── scripts/           # Python scripts for data processing and model training
├── hardware/          # Instructions for hardware setup and wiring diagrams
└── README.md          # Project documentation
