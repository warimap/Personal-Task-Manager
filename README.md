# Personal-Task-Manager
"A user-friendly web application where users can manage tasks by creating, viewing, updating, and deleting them. Each task has a title, description, priority level, and due date."
# Personal Task Manager

## Overview
The Personal Task Manager is a simple web application that allows users to manage their tasks effectively. It provides CRUD (Create, Read, Update, Delete) operations to add, view, edit, and delete tasks. Each task includes details such as a title, description, priority, and due date.

## Features
- Add tasks with title, description, due date, and priority.
- View all tasks in an organized table.
- Edit task details.
- Delete tasks.
- Tasks are ordered by due date and priority.

## Technologies Used
- **Backend:** Flask (Python)
- **Frontend:** HTML, CSS, JavaScript
- **Database:** SQLite

## Project Structure
```
personal_task_manager/
├── app.py
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── add_task.html
│   ├── edit_task.html
├── static/
│   ├── styles.css
├── tasks.db
```

## Setup and Installation

### Prerequisites
- Python 3.x installed
- Flask installed (`pip install flask`)

### Steps
1. Clone the repository or create the file structure as shown above.
2. Navigate to the project directory:
   ```bash
   cd personal_task_manager
   ```
3. Initialize the database:
   ```python
   python -c "from app import init_db; init_db()"
   ```
4. Run the application:
   ```bash
   python app.py
   ```
5. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

## Troubleshooting

### Error: `ERR_CONNECTION_REFUSED`
If you cannot access the app in your browser, follow these steps:

1. **Bind Flask to all interfaces:**
   Update the `app.run()` command in `app.py` to:
   ```python
   app.run(debug=True, host='0.0.0.0')
   ```

2. **Check Port Mapping:**
   If you're using Docker, ensure you map port `5000` in the container to your host machine:
   ```bash
   docker run -p 5000:5000 your_image_name
   ```

3. **Firewall Settings:**
   Ensure your firewall or network settings allow access to port `5000`.

4. **Access the App Correctly:**
   - For local environments, use `http://127.0.0.1:5000` or `http://localhost:5000`.
   - For Docker containers, use the host machine's IP address or the mapped port.

## How to Use

### Add Task
1. Click on the "Add Task" link.
2. Fill out the task details (title, description, due date, priority).
3. Click "Add Task" to save the task.

### View Tasks
The homepage lists all tasks in a table, ordered by due date and priority.

### Edit Task
1. Click the "Edit" link next to a task.
2. Update the task details.
3. Click "Update Task" to save the changes.

### Delete Task
Click the "Delete" link next to a task to remove it from the list.

## Future Enhancements
- User authentication for personalized task management.
- Task categories and tags for better organization.
- Notifications or reminders for due tasks.

## License
This project is open-source and free to use.

## View the Website 
https://personal-task-manager-w4fo.onrender.com
---

### Author
**Faith Warima Ngendo (aka Pharium Warima)**

For questions or feedback, feel free to reach out!
