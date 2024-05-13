#Use Python as base image
From python:3.8-slim-buster

#Set working Directory
WORKDIR /app

# Copy the requirements and install dependencies
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

#Copy the flask application
COPY . /app

#Start Gunicorn
CMD ["gunicorn","--workers", "1", "--bind", "0.0.0.0:8000", "humangov:app"]

