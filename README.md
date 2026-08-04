# Coding Platform Database

A relational database model for an online competitive coding platform, including users, problems, submissions, contests, discussions, and analytics queries.

## 📌 Project Overview

This project designs and demonstrates a full SQL database schema for a coding platform (similar in spirit to Codeforces/LeetCode-style systems). It includes:

- **Schema definition (DDL)**
- **Sample dataset inserts (DML)**
- **Prewritten analytical SQL queries**
- **ER/Schema diagrams**
- **Project documentation PDFs**

---

## 🧱 Database Features

The schema models core platform entities and their relationships:

- **Users** and social graph (`friend_of`)
- **Problems** with tags, favorites, test cases, and expected outputs
- **Submissions** with verdicts, runtime, memory, and language
- **Official solutions**
- **Contests**, participation, and contest authorship
- **Discussions** and discussion posts linked to problems

### Main tables

- `users`
- `friend_of`
- `problems`
- `tags`
- `favorites`
- `test_cases`
- `output`
- `submissions`
- `solution`
- `contests`
- `participates_in`
- `written_by`
- `discussions`
- `about`
- `posts`

Schema namespace used: `CodingPlatform`

---

## 📂 Repository Structure

- `DDLscript.txt` — schema creation and constraint definitions
- `INSERT.txt` — sample data insertion script
- `sqlQUERIES.txt` — 20 useful SQL queries for reporting/analysis
- `MODIFIED_ER_project.jpeg` — ER diagram
- `Modified_ProjectSchema.jpeg` — schema diagram
- `Database Scenario Description.pdf` — project scenario description
- `DB_Complete_Report-II.pdf` — detailed report
- `CodingPlatform_DB_Final_Report.pdf` — final report

---

## ⚙️ How to Run

> Recommended DB: **PostgreSQL** (syntax uses schema/search_path, constraints, interval operations, window functions, `STRING_AGG`, etc.)

### 1) Create database

```sql
CREATE DATABASE coding_platform_db;
```

### 2) Connect and run DDL

```bash
psql -d coding_platform_db -f DDLscript.txt
```

### 3) Insert sample data

```bash
psql -d coding_platform_db -f INSERT.txt
```

### 4) Run analysis queries

Open and execute queries from:

- `sqlQUERIES.txt`

---

## 🔍 Example Query Use Cases

The `sqlQUERIES.txt` file includes queries for:

- User leaderboard by rating
- Contest winners and contest leaderboards
- Submission status reports by problem
- Country-wise average user rating
- User submission summaries
- Most favorited problems
- Friends solving common problems
- Most active discussions
- Problems lacking official solutions
- Efficient submissions and upsolving behavior

---

## 🧪 Notes

- The schema enforces referential integrity with foreign keys and cascading actions.
- Submission status constraints were later altered to support realistic verdict types (e.g., `Wrong_Answer`, `TLE`, `MLE`, `Compile_Error`).
- Includes sample data across users, contests, problems, and submissions to support meaningful analytics.

---

## 🚀 Future Improvements

Potential extensions:

- Admin/moderation roles and permissions
- Submission language/runtime benchmarking tables
- Contest registration windows and virtual participation
- Plagiarism detection metadata
- API-friendly migration/versioning setup (e.g., with Flyway/Liquibase)

---

## 👤 Author

**Hriday (hriday211)**  
Repository: https://github.com/hriday211/Coding-Platform-Database
