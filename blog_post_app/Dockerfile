# # pull official base image
# FROM python:3.9.6-alpine

# # set work directory
# WORKDIR /usr/src/app

# # set environment variables
# ENV PYTHONDONTWRITEBYTECODE 1
# ENV PYTHONUNBUFFERED 1

# # install dependencies
# RUN pip install --upgrade pip
# COPY ./requirements.txt .
# RUN pip install -r requirements.txt
# CMD ["python","manage.py"]
# EXPOSE 80


# # copy project
# COPY . .

# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file to the working directory
COPY requirements.txt .

# Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Django project code to the working directory
COPY . .

# Expose port 80 for the Django application
EXPOSE 80

# Define the command to run your Django application
CMD ["python", "manage.py", "runserver", "0.0.0.0:80"]
