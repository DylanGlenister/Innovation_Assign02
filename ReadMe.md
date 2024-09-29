# Computing Technology Innovation Project Assignment 2
## Weather Analysis and Prediction Using Machine Learning

This project is a weather prediction model designed to provide accurate and accessible weather forecasts for cities and towns across Australia. Using historical weather data and machine learning models, it aims to deliver predictions of temperature, rainfall, humidity, and wind speed.

## Features
- **Weather prediction:** Provides forecasts for temperature, rainfall, wind speed, and humidity.
- **Multiple data sources:** Integrates weather data from multiple reliable datasets, including Kaggle and the Australian Bureau of Statistics.
- **Regression modeling:** Implements machine learning models such as Linear Regression and Ridge Regression to predict weather patterns.
- **Interactive web interface (upcoming):** The model will be integrated with a web application for easy accessibility (currently outside the scope of this report).

## Installation

### Requirements
- Python 3.12.x

### Setting Up a Virtual Environment Using VS Code

1. **Install required VSCode extensions**:
- Jupyter
- Python
- Pylance

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

4. **Install required libraries**
	```bash
	pip install pandas numpy matplotlib seaborn scikit-learn
	```

4. **Open VS Code in your project directory**:
	```bash
	code .
	```

5. **Select the Python interpreter** in VS Code:
	- Open [Submission.ipynb](./Submission.ipynb).
	- Select the button in the top right corner labelled "select kernel".
	- Choose the interpreter from your virtual environment (`venv`).

6. Now, you can run your code in the virtual environment from VS Code.

## Data Sources
- [Australian Weather Data](https://www.kaggle.com/datasets/manidevesh/weather-data-set-australia)
- [Australian Weather Observation Data](https://www.kaggle.com/datasets/alcheng10/bom-weather-observation-data-select-stations)

## Usage

The notebook is split into 7 main sections:
- Imports
- Data Processing
- Visualisation
- Clustering Tests
- Training
- Testing
- Using

The only sections required for using the model are **Imports, Training, and Using**. These sections should be run sequentially.

In order to use the model with your own data, you must provide the data as an array, this array should be as follows:  
`[MinTemp, MaxTemp, Rainfall, WindGustSpeed, WindSpeed9am, WindSpeed3pm, Humidity9am, Humidity3pm, Pressure9am, Pressure3pm, Cloud9am, Cloud3pm, Temp9am, Temp3pm, DayIndex, Year, Month, LocationHash] * 14`

The model expects 14 days worth of data, you can modify this by reprocessing the data after changing the `block_size` settings, then re-training the model.

Once you have your data formatted correctly it can be used with either the linear reggression model or the ridge regression mode. It is recommended you use both to get a better understanding of the weather possibilities.

### Information about the required data
- MinTemp: The minimum temperature for the day (C).
- MaxTemp: The maximum temperature for the day (C).
- Rainfall: How much rain fell in the day (mm).
- WindGustSpeed: The maximum gust speed (km/h).
- WindSpeed9am: The rolling average wind speed at 9am (km/h).
- WindSpeed3pm: The rolling average wind speed at 3pm (km/h).
- Humidity9am: The air humidity at 9am (%).
- Humidity3pm: The air humidity at 3pm (%).
- Pressure9am: The air pressure at 9am (millibars).
- Pressure3pm: The air pressure at 3pm (millibars).
- Cloud9am: A rating of the amount of cloud cover at 9am (0-9).
- Cloud3pm: A rating of the amount of cloud cover at 3pm (0-9).
- Temp9am: The temperature at 9am (C).
- Temp3pm: The temperature at 3pm (C).
- DayIndex: The number of days since 01/01/2000.
- Year: What year it is.
- Month: What month it is a a number (1-12).
- LocationHash: See below.

Available locations are and their hashs:
| Location Name | Hash |
| ------------- | ---- |
| **Albury** | *71933764137593* |
| **BadgerysCreek** | *5259200152751195853701821850987* |
| **Cobar** | *289631527282* |
| **CoffsHarbour** | *20870169995263488321729295730* |
| **Moree** | *332582249829* |
| **Newcastle** | *1446157459539604302949* |
| **NorahHead** | *1446876625935419138404* |
| **NorfolkIsland** | *6214287813483005966275060002404* |
| **Penrith** | *22629523177174120* |
| **Richmond** | *5938386883828477540* |
| **Sydney** | *91780841104761* |
| **SydneyAirport** | *6613506588786455884295264236148* |
| **WaggaWagga** | *412642669215945392088929* |
| **Williamtown** | *105674394847416162962077550* |
| **Wollongong** | *412901285343814447230567* |
| **Canberra** | *4855283242169954913* |
| **Tuggeranong** | *102104193191251112593682023* |
| **MountGinini** | *93613637018046560708685417* |
| **Ballarat** | *4783223491991331188* |
| **Bendigo** | *18688873268340591* |
| **Sale** | *1398893669* |
| **MelbourneAirport** | *102877175957242481379666932542330598004* |
| **Melbourne** | *1427707618201802272357* |
| **Mildura** | *21789487469523553* |
| **Nhil** | *1315465580* |
| **Portland** | *5795977089809215076* |
| **Watsonia** | *6296441793180232033* |
| **Dartmoor** | *4927345311697825650* |
| **Brisbane** | *4788005298140966501* |
| **Cairns** | *74085659995763* |
| **GoldCoast** | *1317747731709867160436* |
| **Townsville** | *398734979096122321824869* |
| **Adelaide** | *4712002626301551717* |
| **MountGambier** | *23965091076619910740917708146* |
| **Nuriootpa** | *1447308980326459797601* |
| **Woomera** | *24610847341245025* |
| **Albany** | *71933762825849* |
| **Witchcliffe** | *105674541772571125863573093* |
| **PearceRAAF** | *379659461565072128688454* |
| **PerthAirport** | *24881442790602444328154395252* |
| **Perth** | *345299383400* |
| **SalmonGums** | *393753565276778372885875* |
| **Walpole** | *24595441344539749* |
| **Hobart** | *79643229123188* |
| **Launceston** | *360697648683280118345582* |
| **AliceSprings** | *20247587308915477085567215475* |
| **Darwin** | *75185322944878* |
| **Katherine** | *1390528158032114314853* |
| **Uluru** | *366891856501* |

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
