###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build

RUN apt-get update && apt-get install -y python3

WORKDIR : /cd

COPY . .

RUN gcr.io/distroless/python3

ENTRYPOINT ["python"]

