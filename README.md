day 1 slot 1 — Project Structure Reference

Root Folder: exam_platform/

app/

* main.py
  → entry point of the FastAPI application
  → starts server and registers routes

app/core/

* config.py
  → loads environment variables from `.env`
  → stores settings like DATABASE_URL, SECRET_KEY

* logging.py
  → configures logging system
  → writes logs to `logs/app.log`

app/database/

* base.py
  → defines SQLAlchemy Base class
  → all models inherit from this

* session.py
  → creates database engine
  → manages DB connection sessions

app/models/
→ contains database table models
→ example: user.py, question.py

app/schemas/
→ defines request/response data validation
→ used by FastAPI (Pydantic models)

app/api/

* routes/
  → contains API endpoints
  → example: auth.py, users.py, exams.py

app/services/
→ business logic layer
→ handles operations like scoring, auth, evaluation

alembic/
→ database migration system
→ tracks schema changes over time

logs/

* app.log
  → automatically created log file
  → stores runtime events and errors

.env
→ environment variables
→ secrets and configuration (not committed)

.gitignore
→ tells Git which files/folders to ignore

requirements.txt
→ list of project dependencies
→ used to recreate environment

README.md
→ project documentation
→ explains setup and usage

-----------------------------------------------------------------------------------------------
