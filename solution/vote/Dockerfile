# Using official python runtime base image
FROM python:3.9.1-buster

# TODO: Create an working directory ("/app")
# inside the image where the application
# files can be copied to. On Linux, you can
# create a directory by using
# "mkdir -p /directory/to/create".
# Hint: RUN
# …
RUN mkdir -p /app

# TODO: Switch the context to the newly
# created folder /app.
# Hint: WORKDIR
# …
WORKDIR /app

# TODO: Install our python dependencies.
# Python projects usually store dependency
# libraries inside a "requirements.txt" file.
# That is also the case in this project. Copy
# this file to "/app/requirements.txt".
# Hint: COPY
# …
COPY requirements.txt ./requirements.txt

# TODO: Install the Python dependencies by
# running "pip install -r requirements.txt".
# …
RUN pip install -r requirements.txt

# Copy our code from the current folder to
# /app inside the container.
COPY . /app

# Default command to be run when launching the container
ENTRYPOINT [ "gunicorn" ]
CMD [ "app:app", "-b", "0.0.0.0:80", "--log-file", "-", "--access-logfile", "-", "--workers", "4", "--keep-alive", "0" ]
