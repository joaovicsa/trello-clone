# Use official Python image
FROM python:3.11

# Set the working directory in the container
WORKDIR /app

# Copy requirements file
COPY requirements.txt requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Expose the application port
EXPOSE 8000

# Run migrations and start server
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "config.wsgi:application"]
