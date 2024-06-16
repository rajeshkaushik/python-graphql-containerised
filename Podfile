# Use the official Python image as the base image
FROM python:3.11.9-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file to the container
COPY requirements.txt requirements.txt

# Install dependencies
RUN pip install -r requirements.txt

# Copy the rest of the application code to the container
COPY . .

RUN python manage.py makemigrations
RUN python manage.py migrate

# Specify the command to run your Django app
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
