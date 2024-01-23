###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build

#RUN RUN apt-get update && apt-get install -y python3-pip

#ENV GO111MODULE=off

WORKDIR /app
COPY . /app

############################################
# HERE STARTS THE MAGIC OF MULTI STAGE BUILD
############################################

FROM gcr.io/distroless/python3

# Copy the compiled binary from the build stage
COPY --from=build /app /app
WORKDIR /app

# Set the entrypoint for the container to run the binary
ENTRYPOINT ["python3", "app.py"]

