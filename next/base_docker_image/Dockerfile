FROM python:2
MAINTAINER Lalit Jain, lalitkumarj@gmail.com

# Install MongoDB and its tools
RUN \
	apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6 && \
	echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/3.4 main" > /etc/apt/sources.list.d/mongodb-org-3.4.list && \
	apt-get update -y && \
	apt-get install -y mongodb-org

# Install python dependencies for next_backend
ADD requirements.txt /requirements.txt
RUN pip install -U -r requirements.txt
