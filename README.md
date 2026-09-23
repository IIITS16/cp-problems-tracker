# 📊 CP Problem Tracker

> A full-stack competitive programming problem tracker built with **Flask, SQLAlchemy, SQLite, HTML, CSS, and JavaScript** — designed to help programmers organize, track, and analyze their problem-solving journey.

<p align="center">

**Track Problems • Monitor Progress • Analyze Performance • Improve Consistency**

</p>

---

## 🌟 Overview

**CP Problem Tracker** is a full-stack web application for managing competitive programming problems from platforms such as **Codeforces, LeetCode, and others**.

The project started as a simple CRUD application and evolved into a modular Flask backend with:

* 🔐 Authentication
* 📝 Problem management
* 🔍 Search & filtering
* 📄 Pagination
* ⭐ Favorites
* ✅ Completion tracking
* ⚡ AJAX interactions
* 📊 Progress dashboard
* 🔌 REST-style API

The goal is to provide a centralized workspace where competitive programmers can keep track of what they have solved, what they need to revisit, and how their overall progress is improving.

---

## ✨ Features

### 🔐 Authentication

* User registration
* User login/logout
* Session-based authentication
* Protected user-specific data
* Flask-Login integration

---

### 📝 Problem Management

Create and manage your personal problem collection.

* ➕ Add problems
* ✏️ Edit problems
* 🗑️ Delete problems
* 🎯 Track difficulty
* ⭐ Store problem rating
* 🌐 Track programming platform
* 🔢 Store question/problem number

---

### ⭐ Productivity Tracking

Keep your problem-solving workflow organized.

* ❤️ Mark problems as **Favorite**
* ✅ Mark problems as **Completed**
* 🔄 Quickly update problem status
* 📈 Track overall completion progress

---

### 🔍 Search, Filtering & Sorting

Find problems quickly using multiple filters.

* Search by problem/question number
* Filter by platform
* Filter by difficulty
* Sort by rating
* Pagination for large problem collections

Example:

```text
Platform: Codeforces
Difficulty: Easy
Page: 2
Sort: Rating
```

---

## 📊 Dashboard

The dashboard provides a quick overview of your competitive programming activity.

### Key Statistics

* 📚 Total Problems
* ✅ Completed Problems
* ❤️ Favorite Problems
* 📈 Completion Percentage
* 🕒 Last Activity

This makes it easier to understand your current progress without manually counting solved problems.

---

## 🖥️ Screenshots

### Problem Tracker

<img width="1292" height="873" alt="CP Problem Tracker" src="https://github.com/user-attachments/assets/0200c020-ca5c-4558-9f90-d64d0f28472b" />

---

### Search & Filtering

<img width="1526" height="911" alt="Search and Filtering" src="https://github.com/user-attachments/assets/27de12b2-ecbf-4542-9aee-378163e86906" />

---

### Dashboard

<img width="1784" height="895" alt="Dashboard" src="https://github.com/user-attachments/assets/8a3ac372-17fc-4600-b2b1-4b30c1eb5b71" />

---

## ⚡ User Experience

The frontend uses JavaScript and AJAX to provide a smoother experience.

Instead of reloading the entire page for simple actions:

```text
User Action
     ↓
JavaScript / AJAX
     ↓
Flask Backend
     ↓
Database
     ↓
JSON Response
     ↓
Dynamic UI Update
```

### Examples

* Toggle Favorite without page reload
* Mark a problem as completed instantly
* Display toast notifications
* Dynamically update problem status

---

# 🔌 REST-Style API

The application includes a backend API that exposes problem data as JSON.

This makes the project easier to extend to:

* React applications
* Mobile applications
* Desktop applications
* Analytics tools
* External clients

---

## 📡 API Endpoints

### Get Problems

```http
GET /api/problems
```

Returns the available problems as JSON.

---

### Filtering

```http
GET /api/problems?platform=Codeforces
```

Filter problems by platform.

---

### Filtering + Pagination

```http
GET /api/problems?platform=Codeforces&difficulty=Easy&page=1
```

Example query parameters:

| Parameter    | Description                    |
| ------------ | ------------------------------ |
| `platform`   | Filter by programming platform |
| `difficulty` | Filter by difficulty           |
| `page`       | Select result page             |
| `sort`       | Sort results                   |

---

## 🛠️ Tech Stack

| Technology         | Purpose                     |
| ------------------ | --------------------------- |
| 🐍 **Python**      | Backend programming         |
| 🌶️ **Flask**      | Web framework               |
| 🗄️ **SQLAlchemy** | ORM / database interaction  |
| 💾 **SQLite**      | Database                    |
| 🔐 **Flask-Login** | Authentication              |
| 🌐 **HTML5**       | Frontend structure          |
| 🎨 **CSS3**        | Styling                     |
| ⚡ **JavaScript**   | Dynamic interactions & AJAX |

---

# 🏗️ Architecture

The application follows a modular Flask architecture using **Blueprints**.

```text
                    ┌──────────────────┐
                    │     Browser      │
                    │ HTML/CSS/JS      │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │      Flask       │
                    │     Routes       │
                    └────────┬─────────┘
                             │
             ┌───────────────┼───────────────┐
             ▼               ▼               ▼
        ┌─────────┐     ┌─────────┐     ┌─────────┐
        │  Auth   │     │ Problems│     │   API   │
        │ Routes  │     │ Routes  │     │ Routes  │
        └────┬────┘     └────┬────┘     └────┬────┘
             │               │               │
             └───────────────┼───────────────┘
                             ▼
                    ┌──────────────────┐
                    │   SQLAlchemy     │
                    │       ORM        │
                    └────────┬─────────┘
                             ▼
                    ┌──────────────────┐
                    │      SQLite      │
                    └──────────────────┘
```

---

# 📂 Project Structure

```text
cp-problem-tracker/
│
├── app/
│   ├── __init__.py
│   ├── models.py
│   ├── extensions.py
│   │
│   ├── routes/
│   │   ├── main.py
│   │   └── auth.py
│   │
│   ├── templates/
│   │
│   └── static/
│       ├── css/
│       ├── js/
│       └── images/
│
├── run.py
├── config.py
├── requirements.txt
└── README.md
```

---

# 🚀 Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/YashXTensei/cp-problem-tracker.git
```

---

## 2️⃣ Enter the Project Directory

```bash
cd cp-problem-tracker
```

---

## 3️⃣ Create a Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 4️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 5️⃣ Run the Application

```bash
python run.py
```

---

## 6️⃣ Open the Application

Visit:

```text
http://127.0.0.1:5000/
```

---

# 🧪 Development Workflow

A typical workflow looks like:

```text
Create Account
      ↓
Login
      ↓
Add Problems
      ↓
Search / Filter
      ↓
Mark as Favorite
      ↓
Solve Problem
      ↓
Mark as Completed
      ↓
Monitor Dashboard
```

---

# 🧠 What I Learned

Building this project helped me understand several important full-stack development concepts.

### Backend

* Flask application structure
* Flask Blueprints
* SQLAlchemy ORM
* CRUD operations
* Authentication
* Session management
* REST-styl
