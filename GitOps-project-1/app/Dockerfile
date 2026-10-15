FROM python:3.11-slim

WORKDIR /app

# Dependency caching
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Application code copy
COPY app.py .

# Security: Non-root user
USER 10001

EXPOSE 5000

CMD ["python", "app.py"]