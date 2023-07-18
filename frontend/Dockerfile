# Use an official Python runtime as the base image
FROM python:3.9

# Set a custom working directory
WORKDIR /app

# Copy the requirements.txt file to the working directory
COPY requirements.txt .

# Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code to the working directory
COPY . .

# Expose the default Flask port (5000)
EXPOSE 5000

# Set the environment variable for Flask
ENV FLASK_APP=app.py

# Start the Flask application
CMD ["flask", "run", "--host=0.0.0.0"]
