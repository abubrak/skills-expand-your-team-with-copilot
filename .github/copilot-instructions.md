### Copilot Instructions

## Project Overview

This is the Mergington High School Management System - a FastAPI-based web application that allows students to view and sign up for extracurricular activities.

**School Details:**
- Name: Mergington High School
- Location: Mergington, Florida (public high school)
- Motto: "Branch out and grow"
- Serves grades 9-12 with 100-150 students per grade
- School year: August to May with 3 trimesters (optional 4th summer cycle)

## Technology Stack

- **Backend:** Python with FastAPI framework
- **Frontend:** HTML, CSS, JavaScript (vanilla)
- **Server:** Uvicorn (ASGI server)
- **Database:** In-memory storage (data resets on server restart)
- **Authentication:** Argon2 for password hashing
- **Additional:** MongoDB support via pymongo

**Important:** Only use HTML, CSS, JavaScript, and Python. No other languages or frameworks.

## Development Environment

For detailed setup instructions, see [docs/how-to-develop.md](../docs/how-to-develop.md).

**Quick Start:**
1. Use GitHub Codespaces for consistent development environment
2. Install dependencies: `pip install -r src/requirements.txt`
3. Run application: `python -m uvicorn src.app:app --host 0.0.0.0 --port 8000`
4. Access at http://localhost:8000 (API docs at /docs)

## Code Architecture

- Keep the directory structure simple and easy to understand
- Do not create long single-file applications
- Do not create additional apps, services, or command-line tools
- The website is for students and teachers - prioritize simple user experience
- All code must be maintainable by non-technical staff

**Directory Structure:**
```
src/
├── app.py              # Main FastAPI application
├── backend/            # Backend logic
│   ├── database.py     # Database operations
│   └── routers/        # API route handlers
└── static/             # Frontend files (HTML/CSS/JS)
```

## Code Style & Quality

- Write simple, maintainable code that non-technical staff can understand
- Avoid software jargon in comments and documentation
- Isolate functions involving grades, scores, or numerical data
- Add unit tests for critical numerical calculations
- Follow Python best practices (PEP 8)

## Security Considerations

- Personal information is processed - prioritize privacy and security
- Never hardcode secrets, passwords, or sensitive information
- Use environment variables or secure prompts for credentials
- Implement proper authentication with login/logout functionality
- Use Argon2 for password hashing (already available in dependencies)

## Documentation

- Always update README.md to explain how to use the program
- Assume users will quickly forget - good documentation is critical
- When README gets too long, organize content into the docs/ directory
- Explain features in simple terms for non-technical users

## Testing

- No existing test infrastructure - tests are optional for minimal changes
- If adding tests, use pytest and follow existing Python testing patterns
- Focus tests on critical functions (especially grade/score calculations)
