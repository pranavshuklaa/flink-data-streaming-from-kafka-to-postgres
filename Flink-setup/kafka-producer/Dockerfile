FROM python:3.8-slim

# Copy the requirements.txt file into the image
COPY requirements.txt .

# Install the dependencies listed in requirements.txt
RUN set -ex; \
    pip install --no-cache-dir -r requirements.txt

# Set the working directory
WORKDIR /

# Copy the wait-for-it.sh script into the image
COPY wait-for-it.sh wait-for-it.sh

# Add the Python producer script to the image
ADD python-producer.py .

# Specify the command to run when the container starts
CMD ./wait-for-it.sh -s -t 30 $ZOOKEEPER_SERVER -- ./wait-for-it.sh -s -t 30 $KAFKA_SERVER -- python -u python-producer.py
