# Cyberpunk To-Do List App

## Description
The **Cyberpunk To-Do List App** is a sleek and futuristic task management tool. Designed with a cyberpunk theme, this app helps you manage tasks with style. It uses Flask for the backend, SQLite for the database, and a modern cyberpunk-styled frontend.

---

## Features
- Add, delete, and display tasks.
- Cyberpunk-themed user interface with neon effects.
- Persistent storage using SQLite.
- Dynamic updates to the task list without refreshing the page.

---

## Project Structure
```
/todo-app
    /app.py              # Main Flask app
    /static              # Static files for frontend
        /css
            style.css    # Styling for the app
        /js
            script.js    # JavaScript logic
    /templates           # HTML templates
        index.html       # Main HTML file
    requirements.txt     # Dependencies
    database.db          # SQLite database
```

---

## Prerequisites
- Python 3.8+
- Pip (Python package manager)

---

## Installation

### 1. Clone the Repository

git clone https://github.com/Levi-Adrid/Des-todo-app.git
cd to-do app
```

### 2. Set Up the Virtual Environment (Optional but Recommended)

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

pip install Flask==2.3.0
pip install Flask-SQLAlchemy==3.0.0
pip install Flask-CORS==4.0.0

```

### 4. Initialize the Database
The database will be created automatically when the app starts, but you can initialize it manually:

python app.py
```

### 5. Run the Application

python app.py
```
Access the app in your browser at: `http://127.0.0.1:5000`

---

## Usage

### Add a Task
1. Enter the task title and an optional description.
2. Click the "Add Task" button to save the task.

### View Tasks
- All tasks are displayed in the task list section.
- Tasks are fetched dynamically from the server.

### Delete a Task
- Click the "Delete" button next to a task to remove it from the list and the database.

---

## Project Files

### Backend
- **`app.py`**:
  - Serves the frontend HTML and static files.
  - Provides RESTful endpoints for managing tasks (`/tasks`).

### Frontend
- **`index.html`**:
  - Main webpage layout.
- **`style.css`**:
  - Cyberpunk-themed styles with neon glow effects.
- **`script.js`**:
  - Handles dynamic task loading and submission.

### Database
- **`database.db`**:
  - SQLite database for storing tasks.

---

## API Endpoints

### GET `/tasks`
- Fetches all tasks from the database.
- **Response**:
```json
{
  "tasks": [
    {"id": 1, "title": "Task 1", "description": "Description 1", "completed": false},
    ...
  ]
}
```

### POST `/tasks`
- Adds a new task to the database.
- **Request Body**:
```json
{
  "title": "Task Title",
  "description": "Optional Description"
}
```
- **Response**:
```json
{
  "message": "Task created",
  "id": 1
}
```

### DELETE `/tasks/<id>`
- Deletes a task by its ID.
- **Response**:
```json
{
  "message": "Task deleted"
}
```

---

## Known Issues
- Ensure the Flask server is running to avoid `404` errors.
- Use a modern browser to experience full styling effects.

---

## Future Enhancements
- Add task editing functionality.
- Include user authentication.
- Add categories and due dates for tasks.

---

## License
This project is licensed under the MIT License.

---

## Acknowledgments
- **Font**: [Orbitron](https://fonts.google.com/specimen/Orbitron) from Google Fonts.
- Inspired by the cyberpunk aesthetic and modern web design trends.

---

Enjoy managing your tasks in a futuristic cyberpunk style!

