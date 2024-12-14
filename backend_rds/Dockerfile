# Вибираємо офіційний базовий образ Python
FROM python:3.11-slim

RUN apt-get update && \
    apt-get install -y libpq-dev gcc && \
    rm -rf /var/lib/apt/lists/*

# Встановлюємо робочу директорію всередині контейнера
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Відкриваємо порт, на якому бу
EXPOSE 8001

CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]