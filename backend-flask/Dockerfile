FROM python:3.10-slim-buster

# Inside container
# make a new file inside container
WORKDIR /backend-flask

# Outside container -> Inside container
# this contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Inside container 
# Install the python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside container -> Inside containers
#  . means everything in the current directory
#  first period /backend-flask outside container
#  second period /backend-flask inside container
COPY . .

# Set environment variables (Env Vars)
# Inside container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (command)
# export FRONTEND_URL="*"
# export BACKEND_URL="*"
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]