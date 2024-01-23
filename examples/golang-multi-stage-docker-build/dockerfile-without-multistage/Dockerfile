###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build

RUN apt-get update && apt-get  -y install openjdk-11-jdk

WORKDIR : /cd

COPY . .

#RUN pip install -r requirements.txt

ENTRYPOINT ["java11", "app.py"]

