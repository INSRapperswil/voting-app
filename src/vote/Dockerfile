# Using official python runtime base image
# TODO: Find the newest official python Docker image tag and use it in your FROM instruction. Format: FROM <imagename>:<tagname>
...

# Set the application directory
# TODO: Create an working directory ("/app") inside the image where the applicaiton files can be copied to. In Linux you can create a directory by using "mkdir -p /diectory/to/create".
...
# TODO: Switch the context to the WORKDIR /app.
...

# Install our python dependencies
# TODO: Python projects usually store dependency libraries inside an "requirements.txt" file. Thats also the case in this project. Copy this file to "/app/requirements.txt".
...
# TODO: Install the Python dependencies by running "pip install -r requirements.txt".
...

# Copy our code from the current folder to /app inside the container
COPY . /app

# Make port 80 available for links and/or publish
# TODO: Expose port 80 so other persons know on this port this Docker service listens on.
...

# Define our default command to be run when launching the container
ENTRYPOINT [ "gunicorn" ]
CMD [ "app:app", "-b", "0.0.0.0:80", "--log-file", "-", "--access-logfile", "-", "--workers", "4", "--keep-alive", "0" ]
