# Use the official Python 3.9 image as the base image
FROM python:3.9-slim-buster

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install the Python dependencies from the requirements file
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code into the container
COPY . .

# Set the environment variables for the application
ENV FLASK_APP=app.py
ENV FLASK_ENV=production

# Expose port 5000 to the host machine
EXPOSE 5000

# Start the Flask web application when the container starts
CMD ["flask", "run", "--host=0.0.0.0"]
