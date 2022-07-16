FROM nginx:latest

# default docker container runs as root user.
RUN apt-get update && apt-get install -y procps

ENV PORT 30015
ENV HOST 0.0.0.0
EXPOSE 30015
