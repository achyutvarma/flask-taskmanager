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
```  <!-- 👈 this closes the bash block -->


###
# Dahboard

<img width="943" height="483" alt="image" src="https://github.com/user-attachments/assets/e69e94bf-025b-4d9a-a855-de16e8e73f5d" />

# Core Models
- User: holds username, password, full name.
- Ticket: tracks tickets with ticket_no, title, description, status, assigned user, comments.
- Comment: linked to tickets — logged by users when updating tickets.
- Task: associated with open tickets, capturing time spent, tool, description, status.

# Usage Flow
- Sign in as a user.
- Navigate to /tickets to see all tickets.
- Create a new ticket via /create_ticket, then view ticket details.
- In the Ticket Detail page:
- Change status or assignee.
- Use the Add Comment section to log notes.

- Go to /tasks/add to create a new task:
  - Select from tickets with statuses other than Closed.
  - Provide description, time spent, tool used, etc.
- Review all tasks on the main /tasks page.

# Development Notes
- Use Flask-Migrate to handle schema changes going forward.
- For production, consider using PostgreSQL or MySQL instead of SQLite.
- Expandable features: user permissions, file attachments preview, email notifications, API endpoints.



