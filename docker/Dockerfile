# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org Flask

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]

#    In this Dockerfile:

#    FROM python:3.8-slim: This line specifies the base image. 
#                          Here, we're using the official Python 3.8 image with a slim Linux distribution as the base.
#    WORKDIR /app: This sets the working directory inside the container to /app.
#    COPY . /app: This copies the current directory (where the Dockerfile is located) into the container's /app directory.
#    RUN pip install --trusted-host pypi.python.org Flask: This installs Flask, a Python web framework, inside the container.
#    EXPOSE 80: This exposes port 80 to allow communication with the Flask application from outside the container.
#    ENV NAME World: This sets an environment variable named NAME with the value World.
#    CMD ["python", "app.py"]: This specifies the command to run when the container starts. 
#                              In this case, it runs the app.py Python script using the Python interpreter.

#    To use this Dockerfile, you'd need to have a file named app.py in the same directory, 
#    containing your Flask application code. You can then build a Docker image using this Dockerfile and 
#    run containers based on that image.