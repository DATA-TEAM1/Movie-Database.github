# Movie-Database.github

This repository contains our **SQL Week 2 Group Project**, focused on building and managing a **Movie Database**.

Each team member is responsible for one key section of the project.  
The goal is to demonstrate solid database design, automation with triggers, reusable SQL logic with functions, and insightful data analytics through queries and reports.

---

## Team Members & Roles (Main Project)

| Member                   | Git Branch              | Part                                  | Role Description                         |
|--------------------------|--------------------------|----------------------------------------|-------------------------------------------|
| Mohammad                 | `feature/constraints`    | Part 1 – Relationships & Constraints   | Handles table relationships and constraints |
| Samuel                   | `feature/triggers`       | Part 2 – Triggers                      | Builds database triggers                   |
| Sayed                    | `feature/views`          | Part 3 – Views                         | Creates SQL views                          |
| Nadya                    | `feature/functions`      | Part 4 – Stored Functions              | Implements stored SQL functions            |
| Nelson (Project Manager) | `feature/analytical`     | Part 5 – Analytical Queries            | Writes analytical SQL queries              |
| Abanoub                  | `feature/reports`        | Part 6 – Reports                       | Generates summary SQL reports              |

---

### 24 November to 1 December Task

Create `server.py` and inside this file create 6 functions to display data from all tables.

Tables: actors, actsin, customers, log_activity, movies, rentings  
Views: view_actor_summary, view_genre_stats, view_movie_summary

---

## Team Members & Roles (Python Tasks)

| Member                   | Git Branch                  | Task Description                                                      | Notes |
|--------------------------|------------------------------|------------------------------------------------------------------------|-------|
| Mohammad                 | `feature/actors`             | Fetch actors table and display results                                |       |
| Samuel                   | `feature/actsin`             | Fetch actsin table and display results                                |       |
| Sayed                    | `feature/customers`          | Fetch customers table and display results                             |       |
| Nadya                    | `feature/log_activity`       | Fetch log_activity table and display results                          |       |
| Nelson (Project Manager) | `feature/movies`             | Fetch movies table and display results                                | OK    |
| Abanoub                  | `feature/rentings`           | Fetch rentings table and display results                              | OK    |
| Krishma                  | `feature/view-actor-summary` | Fetch view_actor_summary view and display results| 

Python Work (Nelson)

For the Python part of the project, I implemented two complete features in their own branches:  
`feature/movies` and `feature/rentings`.
The goal was to create Python scripts that connect to our Supabase PostgreSQL database and display data from specific tables. I used the `psycopg2` library and loaded connection settings securely from a local `.env` file.
**IMPORTANT:**  
The `.env` file **must NOT be uploaded** to GitHub.  
It contains sensitive information (database password, host, and user).  
It should remain **only on your local machine**.
Example structure:
user=YOUR_USER
password=YOUR_PASSWORD
host=YOUR_HOST
port=5432
dbname=postgres
sslmode=require

### 1. Movies Feature (`feature/movies`)
I created the script:
feature_movies/server.py

This script:
- Loads environment variables from `.env`
- Connects to the Supabase database
- Runs a `SELECT * FROM public.movies;` query
- Prints all movie records in the terminal
Main function:
python
get_all_movies()
This function retrieves and displays all rows from the movies table.

2. Rentings Feature (feature/rentings)
I also created the script:
feature_rentings/server.py
This script:
Loads environment variables from .env
Connects to the Supabase database
Executes SELECT * FROM public.rentings;
Prints all renting records in the console

Main function:
python
get_all_rentings()
This function retrieves all rows from the rentings table and prints them in a readable format.

How to Run My Scripts
From the project root:

Run the movies script:
Copy code
python feature_movies/server.py

Run the rentings script:
Copy code
python feature_rentings/server.py
