FROM mongo

MAINTAINER JesusAGC

RUN apt-get update && apt-get upgrade -y

RUN apt-get install python3.7 -y

RUN apt install python3-pip -y

RUN pip3 install pymongo

RUN mkdir mongo_app

WORKDIR /root/mongo_app

COPY populate.py .

COPY find.py .

COPY py_scripts.sh .

RUN ["chmod", "+x", "py_scripts.sh"]

#CMD [ "./py_scripts.sh" ]

EXPOSE 27017



