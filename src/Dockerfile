FROM python:3.8-slim-buster

WORKDIR /app
#Define workspace

COPY requirements.txt /app
#Copy the package need to execute the application (similar to package.json in a node application)

RUN python -m pip install -r requirements.txt
#Similar to npm install but in a python application

COPY . /app
#Copy everything to the VM /app folder

EXPOSE 5000
# Define the port to expose

CMD [ "gunicorn" , "--workers=3", "--bind", "0.0.0.0:5000", "app:app" ]
#Command to initialize the application (gunicorn - Servidor HTTP para rodar a app)