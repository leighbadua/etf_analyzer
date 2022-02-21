# etf_analyzer
An analysis of ETF data that a SQL database stores. This notebook consists of four stocks: GDOT, GS, PYPL, and SQ. Each stock has its own table in the `etf.db` database. Analyze the daily returns of the ETF stocks both individually and as a whole. Then deploy the visualizations to a web application by using Voilà library. 

This project is  divided into the following parts:

* Analyze a single asset in the ETF

* Optimize data access with Advanced SQL queries

* Analyze the ETF portfolio

* Deploy the notebook as a web application using Voilà library.


## Technologies

Click on the links below for documentation on each of the technologies used. This project uses the following libraries and dependencies:
+ [**Anaconda**](https://docs.anaconda.com/): an open source package and environment management system.
+ [**JupyterLab**](https://jupyterlab.readthedocs.io/en/stable/): an extensive environment using web-based user interface designed for data analysis. 
+ [**Pandas**](https://pandas.pydata.org/docs/getting_started/index.html): (included in Anaconda) a Python package data analysis toolkit.
+ [**hvPlot**](https://hvplot.holoviz.org/) and [**GeoViews**](https://pypi.org/project/geoviews/) incorporated into this project. 
+ [**Numpy**](https://numpy.org/doc/stable/) for scientific computing such as mathematical, basic statistical operations, and much more. 
+ [**SQLAlchemy**](https://docs.sqlalchemy.org/en/14/) (included in Anaconda) is an open-source SQL library designed to ease communication between Python-based programs and databases. 
+ [**Voilà**](https://voila.readthedocs.io/en/stable/) allows you to convert a Jupyter Notebook into an interactive dashboard that allows you to share your work with 


## Installation Guide
Check to ensure that Jupyterlab is installed on your machine by entering the following into your environment using `conda list`. If any of these techologies are not installed into your environment, use the corresponding codes in your terminal: 

```
conda install -c pyviz hvplot geoviews
pip install SQLAlchemy
conda install -c conda-forge voila
```

### Instructions to Use JupyterLab

To launch JupyterLab:
  1. Open terminal window, and type `conda activate dev`.
  2. Type `jupyter lab`. JupyterLab user interface should open in your browser. 
      a. Or copy and paste one of the URLs: "http://localhost:8888/lab?token=..." into web browser. 

To exit JupyterLab:
  1. On your web browser, use the Run button to shut down any running kernel sessions.
  2. On the menu bar, on the File menu, select Shut Down. 
  3. Okay to close tabs once a dialog box with "Server stopped" message indicates the server has stopped. 
  4. Navigate to terminal window, where you launched JupyterLab and type `conda deactivate`. This will return you to your `base` environment. 

## Usage

1. Clone the repository 
2. Using your terminal, activate the environemnt and launch jupyter lab (instructions mentioned above).


3. ETF Analyzer on Jupyter Lab:
![image](https://user-images.githubusercontent.com/96001018/154873135-bdebb7ba-9304-4d3d-8705-24351f0c18ee.png)

* Analyze a single asset in the ETF
  * Using a SQL statement to execute a query that reads PYPL data from the database into a Panda DataFrame.
  * Uses `head` and `tail1 functions to review the first and last five rows of the DataFrame. 
  * Created an interactive visualization for PYPL Daily Returns using hvplot. 
  * Created an interactive visualization for PYPL Daily cumulative returns using hvplot.

* Optimize data access with Advanced SQL queries
  * Using advance SQL queries to optimize the efficiency of accessing the data from the database. Select dates where the PYPL closing price was greater than 200.0
  * Find the top ten daily returns for PYPL. 

* Analyze the ETF portfolio
  * Build the entire ETF portfolio and then evaluate its performance. 
  * Use SQL joins to combine all the data for each asset to build the portfolio. 
  * Create a DataFrame and calculate the average daily returns for all four assets. 
  * Using the DataFrame to calculate the annualized returns for the portfolio. 
  * Uses hvplot to visualize the cumulative return values of the ETF values.

4. Deploy the notebook as a web application using Voilà library.
    * To deploy the jupyter notebook as a web application, use the following code into your terminal (after cloning and `cd` into the repository location):
  `voila etf_analyzer.ipynb`
  
 Below are images of the web application using Voila:
 
![image](https://user-images.githubusercontent.com/96001018/154877305-ed2f12f1-74a2-44b7-abea-d41ca9d08a01.png)
![image](https://user-images.githubusercontent.com/96001018/154877363-485be7de-77ff-4f27-bd43-a705c22c8807.png)
![image](https://user-images.githubusercontent.com/96001018/154877452-5db093e3-67bb-4406-85ca-ae890fdccbe2.png)
![image](https://user-images.githubusercontent.com/96001018/154877509-ac5a7334-39b3-4dbb-b7a8-5265d1d20cc7.png)


 ## Contributors

Leigh Anne Badua leighbadua@gmail.com 



## License

+ [GNU General Public License v3.0](https://choosealicense.com/licenses/gpl-3.0/)
 
