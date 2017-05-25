# Use an official ubuntu runtime as a base image
FROM ubuntu:latest

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

RUN apt-get -qq update
RUN apt-get update & apt-get -y install python-pip python-dev build-essential python-tk libhdf5-dev
RUN pip install --upgrade pip
# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt

# Make port 80 available to the world outside this container
#EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
#CMD ["python", "opt/spikefinder/src/convi.py"]
CMD ["python", "convi.py"]

