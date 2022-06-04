FROM python:latest


#Labels as key value pair
LABEL Maintainer="saurabhsamarjeet@gmail.com"

RUN python -m pip install --upgrade pip && python -m pip install psutil && python -m pip install flask && python -m pip install flask_cors

WORKDIR D:\Project\react\api

#to COPY the remote file at working directory in container
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY app.py ./

# Now the structure looks like this '/usr/app/src/test.py'


#CMD instruction should be used to run the software
#contained by your image, along with any arguments.

CMD [ "python", "./app.py"]