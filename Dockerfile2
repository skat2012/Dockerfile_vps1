FROM ubuntu:18.04
RUN apt update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -q python-all python-pip 
RUN rm -rf /tmp/
ADD requirements.txt /tmp/
RUN rm -rf /opt/webapp/
ADD app.py /opt/webapp/
RUN pip install -qr /tmp/requirements.txt
EXPOSE 5000
CMD ["python", "/opt/webapp/app.py"]