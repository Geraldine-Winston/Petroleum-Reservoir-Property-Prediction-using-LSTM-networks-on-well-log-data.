# Petroleum Reservoir Property Prediction using LSTM Networks on Well Log Data

This project applies **LSTM (Long Short-Term Memory) networks** to predict petrophysical properties such as **porosity** from sequential well log data, improving reservoir characterization and aiding decision-making in petroleum engineering.

## Project Overview

- **Input**: Sequential well log features (e.g., Gamma Ray, Resistivity, Density, Neutron Porosity) versus Depth.
- **Target**: Petrophysical property (e.g., Porosity).
- **Model**: LSTM network trained to capture sequential patterns in well logs.
- **Output**: Predicted porosity values along the depth of the well.

## Project Structure

```
📁 Petroleum-Reservoir-Property-Prediction
├── well_log_data.xlsx            # Synthetic well log dataset
├── lstm_well_log_model.pth        # Trained LSTM model weights
├── reservoir_prediction.py       # Main training and evaluation script
├── README.md                      # Project documentation
├── requirements.txt               # Python dependencies
└── .gitignore                      # Files to ignore in version control
```

## Requirements

Install all necessary dependencies using:

```bash
pip install -r requirements.txt
```

**Dependencies:**

```
pandas
numpy
torch
scikit-learn
openpyxl
```

## How to Run

1. Ensure `well_log_data.xlsx` is in the project directory (or generate your own LAS dataset).
2. Run the training script:

```bash
python reservoir_prediction.py
```

3. After training:
   - Model evaluation metrics (MSE and R² Score) will be printed.
   - The trained model will be saved as `lstm_well_log_model.pth`.

## Dataset Example

```csv
Depth,GammaRay,Resistivity,Density,NeutronPorosity,Porosity
1000.0,94.56,123.45,2.45,0.22,0.39
1002.0,87.23,98.76,2.53,0.25,0.41
...
```

## Model Performance

The LSTM model achieves:
- **Test MSE**: ~0.0004
- **Test R² Score**: ~0.89

*(Values may vary slightly depending on random initialization.)*

## Acknowledgements

- Inspired by real-world applications of machine learning in reservoir characterization.
- Future enhancements include multi-property prediction (e.g., permeability, water saturation) and integration with real LAS files.

## Author

**Ayebawanaemi Geraldine Winston**

