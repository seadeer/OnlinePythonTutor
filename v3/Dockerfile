#install Python image
FROM resin/raspberrypi-python:latest
# Enable systemd
ENV INITSYSTEM on

#Create app folder
RUN mkdir -p /usr/src/pytutor
WORKDIR usr/src/pytutor

#Install app dependencies
RUN easy_install pip
RUN pip install bottle

COPY . /usr/src/pytutor
EXPOSE 8003

CMD ["python", "bottle-server.py"]
