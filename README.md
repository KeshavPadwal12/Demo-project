# Demo-project

NL2SQL Demo Project
Overview
This project showcases how to convert natural language questions into SQL queries using the mistralai/Mistral-7B-Instruct-v0.3 model hosted on Hugging Face's Inference API. It provides a simple interface for querying a mock database schema and evaluates the generated SQL using a flexible comparison method.
Note on Model Availability
The following models were evaluated but could not be used due to access or runtime issues:
•	tscholak/optimum-nl2sql
•	b-mc2/sqlcoder
•	Salesforce/grappa_large
As an alternative, the project uses:
mistralai/Mistral-7B-Instruct-v0.3, which responded reliably to test prompts.
Setup Instructions
1.	Install Dependencies
Make sure you have Python installed, then run:
pip install requests python-dotenv
2.	Configure API Access
Create a .env file in the project root and include your Hugging Face token:
HUGGINGFACE_API_TOKEN="your_api_token_here"
Running the Example
To run the demo, execute the following:
python nl2sql_demo.py
This will send a set of example questions to the model, extract the SQL output, and evaluate the results.
Evaluation Strategy
•	Metric Used: Loose Token Match
•	Current Accuracy: 70% on the included test cases


