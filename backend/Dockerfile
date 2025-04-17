# Backend Dockerfile
FROM python:3.9-slim

WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt ./
RUN pip install --no-cache-dir Flask==2.3.3

# Copy application code
COPY . ./

EXPOSE 5000
CMD ["python", "app.py"]
