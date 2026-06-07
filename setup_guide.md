# Project Setup

Step 1: Open the Project

Open PyCharm as Administrator.
Open the FoodSupplyChain project folder.

Step 2: Restore Database

Open SQL Server Management Studio (SSMS) as Administrator.

Steps:-\
Restore Database\
Right-click Databases\
Select Restore Database\
Select Device\
Click ...\
Click Add\
Select the provided .bak file\
Click OK until the restore process completes\

After successful restoration, the FoodSupplyChain database should appear under Databases.\

Step 3: Verify Database Server Name

Open:\
constants.py

Verify that the SQL Server name matches the SQL Server instance name shown in SQL Server Management Studio (SSMS).\

Example:
SERVER_NAME = "YOUR_SERVER_NAME"

If already configured, no changes are required.

Step 4: Configure Ganache

Open Ganache as Administrator\
Click Quickstart\
Open Settings\
Click Add Project\
Browse to:\
FoodSupplyChain-Truffle/truffle-config.js\
Select the file\
Click Save and Restart

Ganache is now linked to the blockchain project.

# Smart Contract Deployment

Step 5: Open Command Prompt

Run Command Prompt as Administrator.

Navigate to the Truffle project:

D:
cd FoodSupplyChain
cd FoodSupplyChain-Truffle

Step 6: Install Truffle

Install Truffle globally:

npm install -g truffle

Step 7: Compile Smart Contracts

Compile blockchain contracts:

truffle compile

Successful compilation generates contract artifacts.

Step 8: Deploy Smart Contracts

Deploy contracts to Ganache:

truffle migrate

<img width="600" height="300" alt="ChatGPT Image Jun 7, 2026, 11_32_20 AM" src="https://github.com/user-attachments/assets/aaab3093-212c-4c01-8851-798cc74ec53e" />


After successful deployment:\
Blocks will be created\
Transactions will appear\
Contract addresses will be generated inside Ganache.\
Configure Contract Address\

Step 9: Identify Blockchain Transaction Table

Open SQL Server:\

FoodSupplyChain Database\
    → Tables

Check the tables and locate the table containing:\
prevhash\
hash\

In this project the table is:\
transaction\

Step 10: Copy Contract Address

Open Ganache.\

Navigate to:\
Transactions\

Copy the Contract Address associated with the deployed transaction contract.\

Step 11: Update constants.py

Open:\

constants.py\

Update:\

CONTRACT_ADDRESS = "PASTE_CONTRACT_ADDRESS_HERE"\

Save the file.\
Run the Application\

Step 12: Start the Server

Open:\

FoodSupplyChainServer.py\

Run the file using PyCharm.\

The server will start and generate a local URL.\

Example:\
http://127.0.0.1:5000\

Step 13: Open Application

Open the generated URL in your browser.\

The login page will appear.\

Login Credentials\

To verify user credentials:\

Open SQL Server\
Expand Tables\

Locate:\
dbo.users\
Right-click\

Select:\
Edit Top 200 Rows\


Default credentials:
this is just a example/default cedentials we had added in this project.\
Email: 1@1.com\
Password: 1\
Use these credentials to access the application.\

Now u will able to acess your project.\
Enjoy exploring your project.\
