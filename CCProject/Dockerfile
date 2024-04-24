FROM python:3.10

# Set working directory
WORKDIR /app

# Copy the contents of the app folder to the container
COPY . /app

# Install required dependencies
RUN pip install --no-cache-dir google-api-python-client google-auth-httplib2 google-auth-oauthlib


# Copy backup script and credentials JSON file into the image
COPY main.py .
COPY credenti.json .


# Run the backup script periodically
CMD ["python3", "main.py"]