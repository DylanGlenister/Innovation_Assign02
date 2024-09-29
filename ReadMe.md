# Computing Technology Innovation Project Assignment 2
## Machine Learning Hell

# Weather Analysis and Prediction Using Machine Learning

This project is a weather prediction model designed to provide accurate and accessible weather forecasts for cities and towns across Australia. Using historical weather data and machine learning models, it aims to deliver predictions of temperature, rainfall, humidity, and wind speed.

## Features
- **Weather prediction:** Provides forecasts for temperature, rainfall, wind speed, and humidity.
- **Multiple data sources:** Integrates weather data from multiple reliable datasets, including Kaggle and the Australian Bureau of Statistics.
- **Regression modeling:** Implements machine learning models such as Linear Regression and Ridge Regression to predict weather patterns.
- **Interactive web interface (upcoming):** The model will be integrated with a web application for easy accessibility (currently outside the scope of this report).

## Installation

### Requirements
- Python 3.x
- Required Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `datetime`, `scikit-learn`

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/DylanGlenister/Innovation_Assign02.git
   cd weather-analysis
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Setting Up a Virtual Environment Using VS Code

1. **Install the Python extension** in VS Code if you haven't already.

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**:
   - On **Windows**:
     ```bash
     .\venv\Scripts\Activate
     ```
   - On **macOS/Linux**:
     ```bash
     source venv/bin/activate
     ```

4. **Open VS Code in your project directory**:
   ```bash
   code .
   ```

5. **Select the Python interpreter** in VS Code:
   - Press `Ctrl+Shift+P` and type "Python: Select Interpreter".
   - Choose the interpreter from your virtual environment (`venv`).

6. Now, you can run your code in the virtual environment from VS Code.

## Data Sources
- [Australian Weather Data](https://www.kaggle.com/datasets/manidevesh/weather-data-set-australia)
- [Australian Weather Observation Data](https://www.kaggle.com/datasets/alcheng10/bom-weather-observation-data-select-stations)

## Usage

1. **Preprocess the data:**
   Ensure that all datasets are processed using the included data processing scripts. Missing values are filled in using interpolation.

2. **Train the model:**
   Use the following command to train the machine learning model:
   ```bash
   python train_model.py
   ```

3. **Make predictions:**
   After training, you can run the prediction script:
   ```bash
   python predict.py
   ```

## Machine Learning Models

### Models used:
- **Linear Regression:** Selected for its simplicity and effectiveness in predicting weather trends.
- **Ridge Regression:** Implemented to compare performance against linear regression.

## Contributing

How to upload files into Github:
1. Add and save the files into the cloned folder in your machine
2. Locate The Source Control tab
3. Enter a message regarding the file that you're going commit
4. Press the commit button
5. Press the button once it shows 'Sync'
6. then push the file to the repository

## Authors

- Dylan Glenister (104875370)
- Alessio Natale (104553948)
- Kanzen Ong (103518124)
