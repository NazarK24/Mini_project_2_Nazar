# Вибираємо офіційний базовий образ Python
FROM python:3.11-slim

# Встановлюємо робочу директорію всередині контейнера
WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Відкриваємо порт, на якому буде працюва
EXPOSE 8001

CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]