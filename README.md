# 🧠 CodeDocGen – Auto Code Documentation Generator

CodeDocGen is a full-stack web application that allows users to upload source code files and automatically generates documentation from them. It uses **Django** as the backend for file handling and parsing, and **React + Vite** as the frontend for user interaction.

## 🔧 Tech Stack

- **Backend**: Django, Django REST Framework, django-cors-headers
- **Frontend**: React + Vite
- **Other Tools**: Python `ast`, axios, PowerShell scripts

## 📁 Project Structure

```
code-docgen/
│
├── backend/                # Django project configuration
│   ├── core/               # Utility code including parser
│   └── settings.py, urls.py, etc.
│
├── core/                   # Django app for handling uploads
│   ├── views.py            # API endpoints
│   └── utils/              # Code parsing utilities
│
├── frontend/               # React + Vite frontend
│   ├── src/                # React source code
│   │   ├── App.jsx         # Main application component
│   │   └── main.jsx        # Entry point
│   └── package.json        # Frontend dependencies
│
├── media/                  # Uploaded code files
├── docs_output/            # Generated documentation
├── env/                    # Python virtual environment (excluded from Git)
└── README.md               # You're reading this!
```

## ⚙️ Setup Instructions

### 1️⃣ Backend (Django)

```bash
# Navigate to project root
cd code-docgen

# Activate virtual environment (Windows)
.\env\Scripts\activate

# Run server
python manage.py runserver
```

📌 Make sure the virtual environment is already set up with:

```bash
# Create virtual environment
python -m venv env

# Install dependencies
pip install django djangorestframework django-cors-headers openai python-magic
```

### 2️⃣ Frontend (React + Vite)

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Run development server
npm run dev
```

## 🚀 How It Works

1. **Upload** any Python code file (.py)
2. **Backend** parses it using Python's `ast` module
3. **Extracts** functions, classes, and docstrings
4. **Frontend** displays markdown-formatted documentation

## 🔄 API Endpoints

- **POST /api/upload/** - Upload a code file and receive generated documentation

## 🔮 Future Enhancements

- Support for more programming languages
- Enhanced documentation with type hints and parameter descriptions
- Bulk file upload support
- Project-level documentation generation
- Customizable documentation templates

## 📝 License

[MIT](https://opensource.org/licenses/MIT)
