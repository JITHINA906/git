FROM ubuntu:latest

# Set the working directory in the image
WORKDIR /test1

# Copy the files from the host file system to the image file system
COPY . /test1

# Install the necessary packages
RUN apt-get update && apt-get install -y python3 python3-pip

# Set environment variables
ENV NAME World

# Run a command to start the application
CMD ["python3", "test1.py"]