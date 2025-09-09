# 📓 CollabNotes – Real-Time Collaborative Markdown Notes App  

A **self-hosted, real-time markdown notes and collaboration app** built with **Flask** and **WebSockets**.  
Multiple users can create, edit, and chat on notes simultaneously – think of it as a lightweight, Python-powered version of Notion/Google Docs.  

---

## ✨ Features  

- 📝 **Markdown Notes** – Create, edit, and delete notes in `.md` format.  
- 🔄 **Real-Time Collaboration** – Live updates using **Flask-SocketIO**.  
- 💬 **Live Chat** – Chat inside each note while editing.  
- 👥 **User Accounts** – Signup/login with role-based access (Owner, Editor, Viewer).  
- 📂 **File Operations** – Notes stored as files, metadata in SQLite.  
- 📜 **Version History** – Track changes across edits.  
- 📑 **Export Options** – Export notes as **PDF/HTML**.  
- 🔎 **Search** – Full-text search across notes.  
- 🖥️ **CLI Tool** – Manage notes from terminal (`uv run collabnotes cli list`).  
- 🧪 **Tests** – Unit + integration tests with `pytest`.  
- 🛠️ **Logging & Config** – Structured logging + YAML-based app config.  

---

## 🏗️ Tech Stack & Python Concepts  

### **Frameworks & Libraries**  
- [Flask](https://flask.palletsprojects.com/) – Web framework  
- [Flask-SocketIO](https://flask-socketio.readthedocs.io/) – Real-time sockets  
- [SQLAlchemy](https://www.sqlalchemy.org/) – ORM for SQLite/Postgres  
- [Markdown](https://python-markdown.github.io/) – Convert `.md` → HTML  
- [WeasyPrint](https://weasyprint.org/) – Export notes to PDF  
- [Click](https://click.palletsprojects.com/) – CLI commands  
- [PyYAML](https://pyyaml.org/) – Config management  
- [pytest](https://docs.pytest.org/) – Testing framework  

### **Concepts Covered**  
- Object-Oriented Programming (`User`, `Note`, `NoteManager`, `ChatRoom`)  
- File operations (read/write `.md`, logs, exports)  
- REST API + Socket events  
- Authentication & sessions  
- Configurable architecture (YAML-based settings)  
- Logging & error handling  
- Unit & integration testing  
- CLI utilities  

---

collabnotes/
├── pyproject.toml          # uv project config
├── app.py                  # Flask entry point
├── config.yaml             # App settings
│
├── collabnotes/            # Main package
│   ├── __init__.py
│   ├── models/             # OOP classes
│   │   ├── user.py
│   │   ├── note.py
│   │   ├── chat.py
│   │
│   ├── services/           # Business logic
│   │   ├── note_manager.py
│   │   ├── auth_service.py
│   │   ├── export_service.py
│   │
│   ├── routes/             # Flask routes
│   │   ├── api.py
│   │   ├── web.py
│   │   ├── sockets.py
│   │
│   ├── utils/              # Helpers
│   │   ├── file_utils.py
│   │   ├── logger.py
│   │
│   └── templates/          # HTML templates
│       ├── base.html
│       ├── notes.html
│       ├── chat.html
│
├── tests/                  # Tests
│   ├── test_api.py
│   ├── test_sockets.py
│   ├── test_notes.py
│
└── static/                 # CSS, JS


# Create a new environment
uv venv

# Activate environment
source .venv/bin/activate   # Linux/Mac
.venv\Scripts\activate      # Windows

# Install dependencies
uv pip install -r requirements.txt


# 📦 Dependencies

Add these to requirements.txt (or pyproject.toml):

flask
flask-socketio
eventlet
sqlalchemy
markdown
weasyprint
click
pyyaml
pytest


🚀 Usage
Run the Flask server

uv run app.py


## 📂 Project Structure  

