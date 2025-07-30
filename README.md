# Flask Task Manager

A lightweight task and ticket management web application built with Flask, SQLAlchemy, and SQLite.

## 🚀 Features

- Create tickets with **auto-generated ticket numbers**
- Assign tickets to users, track statuses (New, In Progress, On Hold, Closed)
- Add comments/logs to tickets via a detailed view
- Create tasks associated with **open tickets**, tracking:
  - Description
  - Time spent
  - Tool used
  - Assignment and status
- Modern UI using Bootstrap for responsive, clean layouts

## 🧭 Project Structure

```
flask-taskmanager/
├── app.py                 # Main Flask app with routes and models
├── dashboard.db           # SQLite database
├── templates/             # Jinja templates
│   ├── login.html
│   ├── dashboard.html
│   ├── tickets.html
│   ├── create_ticket.html
│   ├── ticket_detail.html
│   ├── tasks.html
│   └── create_task.html
├── static/
│   ├── css/
│   └── js/
└── README.md
```



## 🛠️ Getting Started

### Prerequisites

- Python 3.8+
- `pip` package manager

### Installation

```bash
git clone https://github.com/achyutvarma/flask-taskmanager.git
cd flask-taskmanager
python -m venv venv
source venv/bin/activate        # On Windows use: venv\Scripts\activate
pip install Flask Flask-SQLAlchemy Flask-Migrate

# Run the Application
python app.py

Access at http://127.0.0.1:5000/ and log in with default credentials:
admin / admin123
``` 



