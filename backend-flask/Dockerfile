FROM python:3.10-slim-buster

# from outside container folder > into container folder
WORKDIR /backend-flask

#copy libraries used by the app from outside container > into container 
COPY requirements.txt requirements.txt

# install requirements inside container
RUN pip3 install -r requirements.txt

# the first "." is select everything in outside folder the second period is inside container
COPY . .

# Set Environment Variable (En Vars) inside container & will remain there when container is run
ENV FLASK_ENV=development

# Selecting the port to be used by the web server
EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]