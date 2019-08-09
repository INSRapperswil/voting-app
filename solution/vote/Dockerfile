# Using official python runtime base image
FROM python:2.7.16-alpine3.10

# Set the application directory
RUN mkdir -p /app
WORKDIR /app

# Install our python dependencies
COPY requirements.txt /app/requirements.txt
RUN pip install -r requirements.txt

# Copy our code from the current folder to /app inside the container
COPY . /app

# Make port 80 available for links and/or publish
EXPOSE 80

# Define our default command to be run when launching the container
ENTRYPOINT [ "gunicorn" ]
CMD [ "app:app", "-b", "0.0.0.0:80", "--log-file", "-", "--access-logfile", "-", "--workers", "4", "--keep-alive", "0" ]
