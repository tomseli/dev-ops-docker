# FRONTEND
FROM ubuntu:latest

# See readme for port
EXPOSE 5000

# Set workdir
WORKDIR /usr/src/app

# Copy over files
COPY . .

# Get curl
RUN apt update && \
    apt install -y curl

# Instal dependencies
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && \
    apt install -y nodejs && \
    npm install && \
    npm install -g serve

ENV REACT_APP_BACKEND_URL=http://127.0.0.1:8080

RUN npm run build 

ENTRYPOINT [ "serve" ]
CMD ["-s", "-l", "5000", "build"]