# Financial Planning Tool

Financial planning plays an important role in people's financial health. As we get older, it is imperative that we plan for our future beyond our careers. Planning for retirement can be difficult, but with the right tools, it can be as easy as plugging in a few numbers. This financial tool can assist in reaching financial goals by helping find the right investments to build wealth. This financial planning tool will help clients understand their monthly budget in regards to building their retirement portfolio. This tool will also assist in forecasting a reasonably effective retirement plans based on the current portfolio they hold. With the help of this tool, clients will be able to evaluate their financial health, and gain insight on how to plan for the future.

---

## Technologies

In order for this program to run, this application must be used in Jupyter Notebook, as it uses the Pandas/Python language. To run the program, it is essential to have JupyterLab installed. To ensure the code works, please open the file in a dev environment using python. It is also necessary to install Pandas in order to read/run the code.

The operating systems and program versions are mentioned below and are highly recommended when running the program.

**Systems**

[conda 4.10.3](https://docs.anaconda.com/anaconda/install/index.html) - Package manager, Environment Manager

python 3.7 - included in Anaconda

JupyterLab - included in Python 

Pandas - included in Python

[Matplotlib](https://matplotlib.org/stable/users/installing.html) - inlcuded in Python

[Alpaca](https://app.alpaca.markets/login)- Stock trading API that will help supply the application with current and up-to-date information


---

## Installation Guide

As mentioned above, to ensure that there are no errors when running this application, the user or programmer must use JupyterLab to access the application file. 

Additional installs are needed before running the program. Please install in terminal, in a dev environment:

```JupyterLab
conda active dev
python -m ipykernel install --user --name dev
conda install -c conda-forge nodejs
conda deactivate

```
Once installed you should be able to open JupyterLab by the following code:

```
conda activate dev
jupyter lab
```

To exit out of JupyterLab hit: Ctrl + C

It is important to also instal Pandas as the majority of code use is using language from Pandas.

```Pandas
conda activate dev
conda install pandas -y
conda deactive
```

Matplotlib:

```
conda install matplotlib
```


As we are using Alpaca to pull current data, you will need to use your Alpaca key and secret key to pull in the information. This will be housed in a *.env* file. A sample file has been provided, so you can save your keys there to help run the application. This install below will aid in extracting the necessary information from the *.env* file to use Alpaca

```
!pip install python-dotenv
```

The install below will help pull in the Alpaca data.

```
pip install alpaca-trade-api
```


---

## Usage and Examples

To use the financial planning tools, the repository will need to be cloned from GitHub and into a local repository.

Please open the 'final_financial_planning_tools.ipynb' file. Enter into the dev environment by commanding: 

```
 conda activate dev
```
Next, use the code:

```
jupyter notebook
```
to run the file.


When using the file, each line of code must be individually ran to capture the data. This ensures any data that needs to be pulled gets included in future calculations as we start to build out formulas for analysis. It is important that we do not miss a line of code.

To quickly execute the code, use the keyboard shortcut: Shift + Enter.

The most important piece of code we need to run is the imports. Without these, information may not get pulled correctly.


**Creating the Financial Planner**

In this section, we will make API calls to pull the most recent information on Bitcoin and Ethereum. From there, we will used the information pulled to calculate the current value of each of the cryptocurrencies in the portfolio. 

Next, we evaluate the stock and bond in the portfolio. To pull this information, please be sure to have your *.env* file containing keys and secret keys availabe as information from Alpaca will need to be pulled. We will then calculate the current value of the stock and bond.

Together, we sum the two to understand the current value of the portfolio.




**Evaluating an Emergency Fund**

By merging the stock, bond, and cryptocurrencies, a pie chart is generated to give a visual on what the portfolio is composed of. Evaluating the clients portfolio is crutial for clients to determine if they have enough savings to build an emergcy fund into their financial plan. The application tool will advise on what decision to make. The decision making tool built into the application will consider all the data and provide one of three answers: 1) there is enough to start this fund, 2) the financial goal is reached, or 3) the client is XX dollars away from goal.



**Financial Planner for Retirement**

Using the Monte Carlo Simulation (MCForecastTool.py), we are able to use 3 years of historical data to build out 10 year and 30 year portfolio forecasts. By using the simulation and its summary statistics we can provide the client with an expected value of their portfolio from the lower 95% confidence interval to the upper 95% confidence interval. Giving the client this range will provide them with enough information to understand what will be most beneficial in building a retirement fund.


---

## Contributors

[Julia Guanzon](www.linkedin.com/in/julia-guanzon)

## License

GPL-3.0 License
