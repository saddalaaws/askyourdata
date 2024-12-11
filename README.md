Here's a high-level overview of the components and their interactions:

User Interface (Streamlit):

Streamlit App: Provides the user interface for interacting with the application.
Sidebar: Contains options for selecting the AI model, data source, and other features.
API Key Management:

load_api_key: Function to load the API key from a file.
Azure OpenAI Connection:

azureopenai_connection: Sets up the environment variables for connecting to Azure OpenAI.
AWS Athena Connection:

create_athena_connection: Establishes a connection to AWS Athena using the provided connection string.
validate_connection: Validates the connection by querying the list of tables.
SQL Database and Agent:

SQLDatabase: Represents the SQL database connection.
AzureChatOpenAI: Initializes the Azure OpenAI model.
create_sql_agent: Creates an agent for executing SQL queries.
Query Execution:

User Query Input: Users input their queries through the Streamlit interface.
Agent Execution: The agent processes the query and interacts with the SQL database.
Query Results: Results are displayed back to the user.
Here's a visual representation of the architecture:

+-------------------+       +-------------------+
|                   |       |                   |
|   User Interface  |       |  API Key Management|
|   (Streamlit)     |       |                   |
|                   |       |                   |
+---------+---------+       +---------+---------+
          |                           |
          |                           |
          v                           v
+---------+---------+       +---------+---------+
|                   |       |                   |
| Azure OpenAI      |       | AWS Athena        |
| Connection        |       | Connection        |
|                   |       |                   |
+---------+---------+       +---------+---------+
          |                           |
          |                           |
          v                           v
+---------+---------+       +---------+---------+
|                   |       |                   |
| SQL Database      |       | Query Execution   |
| and Agent         |       |                   |
|                   |       |                   |
+-------------------+       +-------------------+
You can use this structure to create a detailed diagram in draw.io. If you need further customization or specific details, let me know
