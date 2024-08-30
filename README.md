# 🌐 Web Scraping on a Schedule with Django and Celery
Learn how to schedule regular web scraping, save the data, and more with Django & Celery.

## Topics:

- 🏗️ Django
- ⏲️ Celery
- 🕷️ Selenium
- 📊 Scraped Data to Database via Django
- 🌐 Reliable Web Scraping with Selenium + Bright Data

## Getting Started 🚀

`macOS/Linux`
```bash
python3 -m venv venv
source venv/bin/activate
```

`Windows`
```bash
c:\Python311\python.exe -m venv venv
.\venv\Scripts\activate
```

Install requirements
```bash
python -m pip install pip --upgrade
python -m pip install -r requirements.txt
```

Run a local Redis instance via Docker Compose
```bash
docker compose -f compose.yaml up -d
```
This will give us `redis://localhost:6170`

Create `.env` in `src/.env` with:

```bash
CELERY_BROKER_REDIS_URL="redis://localhost:6170"
DEBUG=True
```

Navigate into your Django root:

```bash
cd src/
ls
```
You should see at least `scraphome/` and `manage.py`.

Run your project in 2 terminals:
- `python manage.py runserver` 🌟
- `celery -A scraphome worker --beat` 🛠️

Let's go! 🚀
