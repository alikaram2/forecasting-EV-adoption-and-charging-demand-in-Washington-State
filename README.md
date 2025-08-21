EV Charging Data Analysis
This repository contains a Jupyter Notebook (EV_Charging.ipynb) for analyzing electric vehicle (EV) charging data. The project uses Python with popular data science libraries like Pandas, Matplotlib, and Seaborn to process, clean, and visualize the data.

Project Description
The primary goal of this project is to analyze the growth and distribution of electric vehicles within Washington state. The analysis focuses on understanding trends over time and across different counties, with a specific emphasis on Original Title and Transfer Title transactions to estimate the number of EVs on the road. The notebook includes several key steps:

Data Retrieval: The notebook is set up to call an external API and paginate through a large dataset to retrieve information on EV transactions.

Data Cleaning and Preprocessing: The raw data is cleaned by dropping irrelevant columns and handling duplicate entries based on vehicle ID, transaction date, and county. The model column is standardized to ensure consistency.

Exploratory Data Analysis (EDA): The cleaned data is used to generate visualizations that show:

The cumulative number of EVs on the road in Washington state over time.

The total number of EVs by county, highlighting the top 10 most active counties.

The most popular EV models sold in each of the top 10 counties.

Model Fitting: The notebook includes an attempt to fit a SARIMAX model to the data, likely for forecasting future trends, although the code snippet suggests this section is still in development or for demonstration purposes.

Repository Structure
EV_Charging.ipynb: The main Jupyter Notebook containing all the project's code and analysis.

Data/: A directory where the processed data is saved.

title_transactions-{today}.csv.gz: The raw data retrieved from the API, saved as a compressed CSV file.

vehicles_on_the_road-{today}.csv: A processed CSV file used for generating visualizations.

Images/: A directory to store the generated plots and figures from the notebook.

Getting Started
Prerequisites
Python 3.x

Jupyter Notebook or JupyterLab

Required Python libraries:

pandas

requests

matplotlib

seaborn

You can install these libraries using pip:

pip install pandas requests matplotlib seaborn

API Credentials
This project requires API keys to access the data. The notebook assumes that API keys are stored in a json file named api_project.json. The keys should be structured as follows:

{
    "api_key": "YOUR_API_KEY",
    "app_token": "YOUR_APP_TOKEN",
    "api_key_secret": "YOUR_API_KEY_SECRET"
}

Running the Notebook
Clone this repository:
git clone [repository_url]

Navigate to the project directory:
cd [project_directory]

Open the Jupyter Notebook:
jupyter notebook EV_Charging.ipynb

Run the cells in the notebook sequentially to execute the data retrieval, cleaning, and analysis steps.

Analysis Highlights
The project offers valuable insights into the EV market in Washington.

EV Growth Over Time
Top 10 Counties by EV Count
Most Popular EV Models by County
