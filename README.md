# World Capitals Quiz App

A simple web application that tests your knowledge of world capitals. The app is built using Node.js, Express, and PostgreSQL, and uses environment variables for configuration.

## Features

- Serve a quiz asking the capital of a random country.
- Tracks how many answers are correct.
- Uses PostgreSQL to store the list of countries and their capitals.

## Prerequisites

To run this project locally, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v12 or higher)
- [PostgreSQL](https://www.postgresql.org/) (a running instance)
- [Git](https://git-scm.com/) (optional, for cloning the repository)

## Setup Instructions

### 1. Clone the Repository
First, clone the repository to your local machine:
```bash
git clone https://github.com/shirroam/world-capital-quiz.git
```
### 2. Install Dependencies
Install the required Node.js dependencies by running:
```bash
npm install
```
### 3. Configure PostgreSQL
Make sure you have PostgreSQL installed and running. Create a database for the app and a 'capitals' table to store the countries and capitals.

Example SQL to create the table:
```sql
CREATE TABLE capitals (
  id SERIAL PRIMARY KEY,
  country VARCHAR(100),
  capital VARCHAR(100)
);
```
You can now load your data from the provided CSV file (capitals.csv) or manually insert the data into the capitals table.
### 4. Configure Environment Variables
Create a .env file in the root of your project to store your PostgreSQL connection details. Use the .env.example file as a template and replace it with your actual PostgreSQL credentials.

Example .env file:
```bash
PG_USER=your_postgres_username
PG_HOST=localhost
PG_DATABASE=your_database_name
PG_PASSWORD=your_postgres_password
PG_PORT=5432
```
### 5. Start the Server
Run the server with the following command:
```bash
npm start
```
This will start the server at http://localhost:3000.

### 6. View the App
Open your web browser and go to http://localhost:3000. You should see the quiz asking you to name the capital of a random country. Enter your answers, and the app will keep track of your score.
