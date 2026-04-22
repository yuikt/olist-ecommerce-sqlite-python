## olist-ecommerce-sqlite-python

Practice using SQL Views within a Python environment to "querying data" for business data analytics

- Dataset: Olist dataset, a real-world e-commerce dataset from Brazil
- Database: SQL (Ref:https://www.kaggle.com/datasets/terencicp/e-commerce-dataset-by-olist-as-an-sqlite-database/data)
- Language: Python 3.x

### Download SQL database and query data
*sqlite_python_improt_data_ETL*  ----> There are 2 approaches in this script.

Approach 1: 
- Download the Olist SQLite database directly from Kaggle
- Establishes a connection via `sqlite3` and queries data using SQL

Approach 2 - Custom ETL pipeline (CSV to SQL):
- Extract raw .csv files and transform them as `pd.DataFrame`
- Build and connect to an in-memory SQLite database via `sqlite3`
- Convert dataframe to SQL tables with `df.to_sql`
- Write SQL queries as strings and executes them further with `pd.read_sql_query`

### SQL to dataframe and analytical ETL pipeline
*sqlite_python_business_pipeline*
- Download database from kaggle and establish a connection via `sqlite3` to extract tables directly into dataframe.
- SQL Integration: Execute analytical SQL queries by passing multi-line strings and the database connection to `pd.read_sql_query`
- Data Transformation: Convert SQL result sets into dataframe to perform ETL and further business analysis.  
  <u>Credits & References</u>: Data visualization and analysis logic inspired by the notebook [SQL Challenge: E-commerce data analysis](https://www.kaggle.com/code/terencicp/sql-challenge-e-commerce-data-analysis)

### Initial Setup
1. Open terminal (``Ctrl + ` `` for VS Code) and create a virtual envionment (venv). Here we named venv as "venv-olist-sqlitedb"
   ```
   python -m venv venv-olist-sqlitedb
   ```
2. Activate the Environment
   
   Mac/Linux: 
   ```
   source venv-olist-sqlitedb/bin/activate
   ```

   Windows:
   ```
   venv-olist-sqlitedb\Scripts\activate
   ```

3. Install Dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Configure VS Code Interpreter
- Press `Cmd + Shift + P` (or `Ctrl + Shift + P` on Windows) and select "Python: Select Interpreter".
- Choose the one that includes `./venv-olist-sqlitedb/`


### Running this project
- Open terminal (``Ctrl + ` `` for VS Code) and type this command to activate the environment every time you want to run this project.
  ```
  source venv-olist-sqlitedb/bin/activate
  ```
- To stop working, type this command to deactivate.
  ```
  deactivate
  ```
  
