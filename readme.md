# Predictive Analytics Project for Working Capital Optimization
# Project Overview
## Overview
Working capital optimization involves strategically managing a company's current assets
and liabilities to enhance operational efficiency and financial health. It focuses on finding
the right balance between accounts receivable (AR) and accounts payable (AP) to
ensure sufficient liquidity while minimizing costs and risks.
AR data refers to money customers owe the company, while AP data represents the
money the company owes to suppliers.
This involves predicting the timing of customer payments and supplier payments to
ensure cash flow and liquidity in a specific period for the company. By analyzing
historical data and using predictive modeling techniques, the project aims to forecast
the week customers are likely to pay the company and the week in which the company
should pay suppliers.
These predictions enable the company to proactively manage cash flow, ensuring that
customer payments are received on time to cover outgoing payments to suppliers. This
helps maintain a healthy cash position, enhances liquidity, and allows the company to
meet its financial obligations effectively.
Aim
The project aims to optimize working capital management by leveraging accounts
receivable and payable data. Through predictive analysis, the project aims to accurately
forecast the timing of customer and supplier payments, enabling the company to ensure
cash flow and liquidity within a specified period.
## Data Description
● Customer Data:
○ Customer ID: Unique identifier for each customer.
○ Customer Name: Name of the customer.
○ Customer Payment Terms: Terms and conditions for customer payments.
○ Address: Physical address or location of the customer.
○ Credit Limit: Maximum credit amount extended to the customer.
● Receivables Data:
○ Business Code: Code representing the type of business transaction.
○ Customer Number: Unique identifier for each customer.
○ Customer Name: Name of the customer.
○ Payment_Date: Date of payment received.
○ Business Year: Year of the business transaction.
○ Posting_Date: Date of posting the transaction.
○ Due_Date: Date by which the payment is due.
○ Payterm: Payment terms for the invoice.
○ Invoice Currency: Currency in which the invoice is issued.
○ Total Open Amount: Total amount of the invoice.
○ USD_CURRENCY: Currency conversion rate to USD.
○ Total Open Amount_USD: Total amount in USD.
○ Invoice ID: Unique identifier for each invoice.
○ Is Open: Indicates whether the invoice is open or closed.
○ DUNNLEVEL: Dunn level of the invoice. Dunn level refers to the level of
past-due status or aging of an invoice, indicating the severity or length of
time the invoice remains unpaid, basically how many times the customer
was contacted for payment and the status remained unchanged.
○ Credit_limit: Credit limit assigned to the customer.
○ Baseline_Date: Baseline date for the transaction.
○ Region: Geographic region associated with the transaction.
● Suppliers Data:
○ Supplier ID: Unique identifier for each supplier.
○ Supplier Name: Name of the supplier.
○ Payment Terms: Terms and conditions for supplier payments.
○ Vendor Type: Type or category of the vendor/supplier.
○ Supplier Category: Categorization of the supplier.
● Payables Data:
○ Invoice Number: Unique identifier for each invoice.
○ Posting Date: Date of posting the invoice.
○ Invoice Date: Date of the invoice.
○ Payment Date: Date of payment made.
○ Net Due Date (System Calculated Date): Calculated date for net payment
due.
○ Supplier ID: Unique identifier for each supplier.
○ Invoice Amount: Total amount of the invoice.
○ Fiscal Year: Financial year associated with the invoice.
○ Overdue: Indicates if the payment is overdue.
○ Invoice Status: Status of the invoice (e.g., paid, outstanding).
○ Spend Category: Categorization of the expenditure.
○ Total Outstanding Amount: Total amount outstanding for the invoice.
○ Late Payment Fees: Fees charged for late payments.
○ Payterm_n: Payment terms for the invoice.
○ Vendor Type: Type or category of the vendor/supplier.
## Tech Stack
➔ Language: Python
➔ Libraries: pandas, numpy, matplotlib, statsmodels, seaborn, scikit-learn, pyodbc
Approach
● AR Data:
○ Exploratory Data Analysis (EDA): Analyze the accounts receivable data to
gain insights into the distribution, trends, and patterns.
○ Feature Engineering: Transform and manipulate the AR data to extract
relevant features for the prediction model.
○ Model Building: Utilize various regression models such as
RandomForestRegressor, LinearRegression, KNeighborsRegressor,
GradientBoostingRegressor, and SVR to predict the week of customer
payments.
● AP Data:
○ EDA: Perform exploratory analysis on the accounts payable data to
understand its characteristics and identify any anomalies.
○ Feature Engineering: Engineer additional features from the AP data that
may be relevant for the analysis and prediction.
○ Model Building: Develop prediction models based on the AP data to
forecast the week of supplier payments.
● Working Capital Optimization (WCO) Calculations:
○ Group and sum the receivables and payables data on a weekly basis.
○ Calculate the working capital by subtracting the sum of payables from the
sum of receivables for each week.
○ Analyze the working capital figures to identify periods of positive or
negative cash flow and assess the overall liquidity.
## Project Takeaways
1. Develop strong data analysis skills through exploratory data analysis of accounts
receivable and payable data.
2. Gain experience in transforming and manipulating data to create meaningful
features for financial predictive modeling.
3. Build regression models using various algorithms such as
RandomForestRegressor, LinearRegressor, KNeighborsRegressor,
GradientBoostingRegressor, and SVR.
4. Understanding the importance of different features in predicting payment timings.
5. Gain expertise in predicting and forecasting cash flow based on customer
payments and supplier payments.
6. Optimize working capital by analyzing and managing the balance between
accounts receivable and payable.
7. Learn how to communicate the results and insights derived from the predictive
models.
8. Gain practical experience in applying data analysis and predictive modeling
techniques to real-world financial data.
9. Understand financial concepts, working capital management, and its impact on
business performance.








## MS SQL Server Database Set Instructions on AWS RDS

Amazon Web Services (AWS) provides a fully managed Relational Database Service (RDS) that allows you to easily set up and manage MS SQL Server databases in the cloud. In this section, we will walk you through the steps to create an MS SQL Server database on AWS RDS, both using Excel files and .bak files through Amazon S3.

Step 1: Download and Install SQL Server Management Studio (SSMS)
Before setting up the database, you need to have SQL Server Management Studio (SSMS) installed on your local machine. SSMS is a powerful tool for managing and querying SQL Server databases. You can download the latest version of SSMS from the Microsoft website: Download SQL Server Management Studio (SSMS). https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16


Step 2: Install Required Drivers
To connect to the SQL Server database on AWS RDS, you may need to install the necessary drivers on your local machine. 

Microsoft Access Database Engine: If you encounter the error "The 'Microsoft.ACE.OLEDB.16.0' provider is not registered on the local machine" while working with Excel files, you can download and install the Microsoft Access Database Engine from the Microsoft website: Download Microsoft Access Database Engine.

SQL Server Native Client: Install the SQL Server Native Client, which provides connectivity to SQL Server databases. You can download it from the Microsoft website: Download SQL Server Native Client.

ODBC Driver for SQL Server: If you plan to use ODBC to connect to the SQL Server database, you can download the ODBC Driver for SQL Server from the Microsoft website: Download ODBC Driver for SQL Server.

Step 3: Create an MS SQL Server Database on AWS RDS
Sign in to AWS Console: Log in to your AWS account and navigate to the AWS Management Console.

Open RDS Dashboard: Go to the RDS service and open the RDS dashboard.

Launch DB Instance: Click on the "Create Database" button to launch a new DB instance.

Select Engine: Choose "SQL Server" as the database engine.

Choose Use Case: Select the appropriate use case based on your requirements.

Specify DB Details: Provide the necessary details such as DB instance identifier, username, password, and other configuration settings.

Configure Advanced Settings: Customize advanced settings like VPC, security groups, backup retention period, etc.

Create Database: Review your settings and click on "Create Database" to initiate the database creation process.


Step 4: Connect to the MS SQL Server Database


Once the database is created, you can connect to it using SQL Server Management Studio or any other compatible client tool. To do this, you'll need the endpoint and credentials (username and password) you provided during the RDS instance creation.

Obtain Endpoint: In the RDS dashboard, locate your DB instance and note down its endpoint.

Open SSMS: Launch SQL Server Management Studio.

Connect to Database: In SSMS, click on "Connect" and enter the following details:

Server name: Provide the RDS endpoint.
Authentication: Choose "SQL Server Authentication."
Username and Password: Enter the credentials you specified during database creation.
Connect: Click on "Connect" to establish the connection to your MS SQL Server database on AWS RDS.


## Excel File


To upload an Excel file to tables in SQL Server Management Studio (SSMS) using the graphical user interface (GUI), you can follow these steps:
1. Launch SQL Server Management Studio and connect to the SQL Server instance where you want to upload the Excel file.
2. Expand the database node where you want to create the table and right-click on the "Tables" folder. Select "Tasks" and then "Import Data..." from the context menu. This will open the SQL Server Import and Export Wizard.
3. In the wizard, select the "Microsoft Excel" data source as the data source and specify the path to your Excel file.
4. Choose the appropriate Excel version and worksheet from the Excel source. You can preview the data by clicking the "Preview" button to ensure it is correct.
5. Click the "Next" button to proceed to the "Destination" screen. Select the destination database and table where you want to upload the data. If the table does not exist, you can choose to create a new table.
6. Click the "Edit Mappings" button to review and adjust the column mappings between the source and destination. You can modify the data types and other properties if necessary.
7. Once you have reviewed the mappings, click the "Next" button to proceed to the "Specify Table Copy or Query" screen. Here, you can choose to copy data to a new table or append it to an existing table.
8. Review the summary screen and click the "Finish" button to start the import process.
9. The import process will begin, and you can monitor its progress in the wizard. Once the import is complete, you will see a completion screen with the import summary.
10. Finally, you can verify the data by querying the table in SQL Server Management Studio.
By following these steps, you should be able to upload an Excel file to tables in SQL Server Management Studio using the GUI.


### .BAK File

To restore a .bak file from Amazon S3 to an SQL Server database, you can follow these steps:

Upload .bak File to S3: Using the AWS Management Console, navigate to the S3 service and upload the .bak file to a specified S3 bucket.

Open SQL Server Management Studio (SSMS): Launch SSMS on your local machine.

Connect to SQL Server: Connect to the SQL Server instance where you want to restore the .bak file. You can do this by providing the server name, authentication details, and login credentials.

Open Query Window: In SSMS, open a new query window to execute T-SQL commands.

Restore Database: Use the RESTORE DATABASE statement to restore the .bak file into a new or existing database. For example:

```
exec msdb.dbo.rds_restore_database
	@restore_db_name='wco-db1',
	@s3_arn_to_restore_from='arn:aws:s3:::wco-bucket/wcoDB.bak';

    
exec msdb.dbo.rds_task_status @db_name='wco-db1';


```


If you face error while uploading excel -
https://answers.microsoft.com/en-us/msoffice/forum/all/the-microsoftaceoledb160-provider-is-not/45dd60f3-69f5-4e9c-ba8d-2b2bcc4bc78c

sql server native client - https://www.microsoft.com/en-us/download/details.aspx?id=50402

odbc driver for sql server - https://learn.microsoft.com/en-us/sql/connect/odbc/download-odbc-driver-for-sql-server?view=sql-server-ver16
