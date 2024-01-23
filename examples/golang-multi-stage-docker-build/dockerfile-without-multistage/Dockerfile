###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build

RUN apt-get update && apt-get install -y python3-pip

WORKDIR : /cd

COPY . .

#RUN pip install -r requirements.txt

ENTRYPOINT ["python3"]

