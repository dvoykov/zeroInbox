# Telegram Message Categorization Bot
This Telegram bot helps users categorize their saved messages using the OpenAI API, improving their organization and search efficiency.

## Getting Started
To get started with this bot, you'll need to set up a few things:

### 1. Clone the repository:
```python
git clone https://github.com/SimulatorML/zeroInbox.git
```

### 2. Install dependencies:
```python
pip install -r requirements.txt
```

### 3. Set up a PostgreSQL Database:
To use the bot, you need to set up a PostgreSQL database and create a table to store categorized messages. Follow these steps to initialize your database:
* `Install PostgreSQL`: If you haven't already, install PostgreSQL on your system. You can download the installer for your operating system from the [official PostgreSQL website](https://www.postgresql.org/download/).

* `Create a PostgreSQL Database:`: Connect to the PostgreSQL server and create a new database for the project `>>> create database <database_name>;`.
* `Create a Database User (Optional)`: You can create a dedicated database user for the CatBot project with limited permissions. This step is optional but recommended for security reasons. Run the following command in the PostgreSQL shell to create a new user `>>> create user <user_name> with password '<password>';`
* `Create the Table`: Once connected, create a necessary table using the `init_db.sql` script located in `database` folder. Run the following command in the PostgreSQL shell `>>> \i path/to/init_db.sql;`

### 4. Set up environment variables:
Before running the bot, you'll need to set up global environment variables:
* `OPENAI_API_KEY`: Your OpenAI API key. You can get one by signing up at OpenAI.

* `BOT_TOKEN`: Your Telegram bot token. You can create a new bot and get the token from the BotFather.
* `db_host`: The hostname or IP address of the machine where your
PostgreSQL database server is running.
* `db_name`: The name of the PostgreSQL database that your bot will connect to.
* `db_port`: The port number on which your PostgreSQL server is listening.
* `db_user`: The username that your bot will use to authenticate with the PostgreSQL database.
* `db_pwd`: The password associated with the db_user for accessing the PostgreSQL database.

You can set these variables in your system's environment variables or use a tool like dotenv to load them from a file.

### 4. Customize the `prompts.yml` file:
The prompts.yml file contains prompt templates and suggested categories for messages.
You can update entries in this file to customize the prompts and categories used by the bot.

Expected file structure:
```python
msg_classes: <messages categories: List[str]>
msg_classification_prompt: <prompt template: str>
```

### 5. Run the bot:
```bash
./run_bot.sh
```

## Usage
Once the bot is running, users can interact with it to categorize their saved messages.<br>
The bot uses the OpenAI API to analyze messages and suggest categories.

## Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request.<br>
Contributions are always welcome!

## License
This project is licensed under the MIT License - see the LICENSE file for details.