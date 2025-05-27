# Flask ToDo App

A simple and intuitive ToDo application built with Flask, SQLAlchemy, and Bootstrap. This application allows users to manage their daily tasks with basic CRUD operations in a clean, responsive interface.

## Features

- ✅ Add new ToDo items with title and description
- ✏️ Update existing ToDo items
- 🗑️ Delete ToDo items
- 📱 Responsive design with Bootstrap
- 🕒 Automatic timestamp tracking
- 💾 SQLite database for data persistence

## Screenshots

![ToDo App Interface](https://github.com/AdarshXKumAR/To-do-List/blob/main/demo.png)

## Technologies Used

- **Backend:** Flask (Python)
- **Database:** SQLite with SQLAlchemy ORM
- **Frontend:** HTML5, CSS3, Bootstrap 5
- **Template Engine:** Jinja2

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/flask-todo-app.git
   cd flask-todo-app
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install Flask Flask-SQLAlchemy
   ```

4. **Initialize the database**
   ```bash
   python
   >>> from app import app, db
   >>> with app.app_context():
   ...     db.create_all()
   >>> exit()
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Access the application**
   Open your web browser and navigate to `http://localhost:5000`

## Project Structure

```
flask-todo-app/
│
├── app.py                 # Main Flask application
├── database.db            # SQLite database (created after first run)
├── templates/
│   ├── base.html          # Base template
│   ├── index.html         # Home page template
│   └── update.html        # Update ToDo template
├── static/
│   ├── css/
│   │   └── style.css      # Custom CSS styles
│   └── js/
│       └── test.js        # JavaScript files
└── README.md              # Project documentation
```

## Usage

### Adding a ToDo
1. Fill in the "ToDo Title" and "ToDo Description" fields
2. Click the "Submit" button
3. Your new ToDo will appear in the list below

### Updating a ToDo
1. Click the "Update" button next to any ToDo item
2. Modify the title and/or description
3. Click "Update" to save changes

### Deleting a ToDo
1. Click the "Delete" button next to any ToDo item
2. The item will be permanently removed from your list

## Database Schema

The application uses a simple SQLite database with one table:

### Todo Table
| Column | Type | Description |
|--------|------|-------------|
| sno | Integer | Primary key (auto-increment) |
| title | String(200) | ToDo title (required) |
| desc | String(500) | ToDo description (required) |
| date_created | DateTime | Timestamp of creation |

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET/POST | `/` | Home page - displays all ToDos and handles new ToDo creation |
| GET/POST | `/update/<int:sno>` | Update specific ToDo by serial number |
| GET | `/delete/<int:sno>` | Delete specific ToDo by serial number |
| GET | `/show` | Debug endpoint to display all ToDos in console |

## Contributing

1. Fork the repository
2. Create a new feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements

- [ ] User authentication and authorization
- [ ] Categories/tags for ToDos
- [ ] Due dates and reminders
- [ ] Search and filter functionality
- [ ] Export ToDos to different formats
- [ ] Dark mode toggle
- [ ] Priority levels for tasks

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/yourusername/flask-todo-app](https://github.com/yourusername/flask-todo-app)

## Acknowledgments

- [Flask Documentation](https://flask.palletsprojects.com/)
- [Bootstrap](https://getbootstrap.com/)
- [SQLAlchemy](https://www.sqlalchemy.org/)
