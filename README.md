# Business Profile Website (Django)

Minimal, elegant business profile website built with Django and Bootstrap 5.

Requirements
- Python 3.10+
- See `requirements.txt` (Django, Pillow)

Quick start (Windows PowerShell)

1. Create virtualenv and install:

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1; pip install -r requirements.txt
```

2. Apply migrations and create superuser:

```powershell
python manage.py migrate
python manage.py createsuperuser
```

3. Run development server:

```powershell
python manage.py runserver
```

Docker / Deployment

Build and run with Docker:

```powershell
docker build -t business_profile .
docker run -p 8000:8000 business_profile
```

The site includes a dark mode toggle (top-right) which persists the preference using localStorage.

4. Admin: http://127.0.0.1:8000/admin/

Notes
- Static files served via Django staticfiles in development. For production, run `python manage.py collectstatic` and serve `STATIC_ROOT` via your host.
- Update `SECRET_KEY` in `business_profile/settings.py` and set `DEBUG=False` for production.
- Media files (images uploaded for projects/team) are stored in the `media/` folder.

Deployment
- Ready to deploy to Render, PythonAnywhere, or other WSGI hosts. Configure environment variables and static/media hosting per platform.
