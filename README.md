# My To-Do List

This is a simple to-do list web app I made with Django for my in-class assignment. You can add your daily tasks, edit them, mark them as done, and delete them when you don't need them anymore.

## What I did

I built all the things asked in the assignment:

1. **Home page** - a clean page with the title "My To-Do List", an "Add Task" button and a table of all tasks.
2. **Add task** - a form where you enter a title and a description and save the task.
3. **Display tasks** - the table shows the title, description, done status and the date the task was created.
4. **Update task** - the Edit button opens the same form with the old details filled in, so you can change them.
5. **Mark as completed** - there is a small box in the Done column. Click it to mark the task as completed, click again to make it pending.
6. **Delete task** - the Delete button removes the task from the list.
7. **Task status** - completed tasks have a green row and a green tick, and pending tasks have a grey row, so you can tell them apart easily.
8. **Empty state** - when there are no tasks, the page shows "No tasks yet."

## How I built it

- **Django** for the backend
- **HTML and CSS** for the design
- **Django templates** to show the tasks on the page (`base.html`, `task_list.html`, `task_form.html`)
- **Django model** (`Task`) to store the title, description, done status and created date in the database
- **Django form** (`TaskForm`) to take the input for adding and editing tasks
- **URL patterns** for each action (home, add, edit, toggle and delete)
- **POST requests** for creating, updating, completing and deleting tasks. The complete and delete links only work with POST, so opening them directly in the browser doesn't do anything.
- **CSRF protection** added to every form that uses POST


## How to run it

1. Make sure Django is installed:
   ```
   pip install django
   ```
2. Open the project folder in the terminal (the one with `manage.py`)
3. Set up the database:
   ```
   python manage.py migrate
   ```
4. Start the server:
   ```
   python manage.py runserver
   ```
5. Open http://127.0.0.1:8000/ in your browser

## Project files

- `tasks/models.py` - the Task model
- `tasks/forms.py` - the task form
- `tasks/views.py` - the logic for add, edit, complete and delete
- `tasks/urls.py` - the URLs for each page
- `templates/` - the HTML pages
- `static/style.css` - the styling
