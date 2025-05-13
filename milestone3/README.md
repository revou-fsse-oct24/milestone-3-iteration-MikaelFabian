# 🏦 RevoBank API

📊 Overview of the API
<div style="text-align: justify">
RevoBank API is a RESTful API built with Flask that implements core banking features for User Management, Account Management, and Transaction Management. This API serves as the backend for the RevoBank application.
</div>

## Features Implemented
1. User Management
   - Create new users acc
   - Retrieve user profile
   - Update user profile
   - User authentication


2. Account Management
   - Create new bank acc
   - Retrieve & update account details
   - List all accounts
   - Delete account

3. Transaction Management
   - Create transactions (deposit, withdrawal, transfer)
   - Retrieve transaction details
   - List all transactions
   - Filter transactions by account

## Database Schema
FLASK_APP=app
FLASK_ENV=development
DATABASE_URL=sqlite:///revobank.db
JWT_SECRET_KEY=your-super-secret-key-change-this

### Users Table
- `id` (Integer, Primary Key)
- `username` (String, Unique)
- `email` (String, Unique)
- `password` (String, Hashed)
- `created_at` (Timestamp)
- `updated_at` (Timestamp)

### Accounts Table
- `id` (Integer, Primary Key)
- `user_id` (Integer, Foreign Key → Users)
- `account_number` (String, Unique)
- `balance` (Float)
- `created_at` (Timestamp)
- `updated_at` (Timestamp)

## Installation and Setup Instructions
1. Clone the repository
```bash
git clone https://github.com/revou-fsse-oct24/milestone-3-iteration-MikaelFabian
cd milestone3
```

2. Create and activate virtual environment
```bash
uv venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate  # Linux/Mac
```

3. Install dependencies
```bash
uv pip install -r requirements.txt
```

4. Setup environment variables (.env)

5. Run the application
```bash
python main.py
```

The API will be available at `http://localhost:8000`

## Technologies Used
- Flask (Python Web Framework)
- SQLAlchemy (ORM)
- Flask-JWT-Extended (Authentication)
- PostgreSQL (Production Database)
- SQLite (Development Database)