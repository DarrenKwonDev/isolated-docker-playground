FROM nginx:latest

# default docker container runs as root user. don't 
RUN apt update && apt install -y build-essential
# RUN apt-get update && apt-get install procps -y

ENV PORT 30015
ENV HOST 0.0.0.0
EXPOSE 30015
