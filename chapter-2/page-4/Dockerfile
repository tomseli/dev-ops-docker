FROM ubuntu:24.04

WORKDIR /mydir

RUN apt-get update &&\
    apt-get install -y curl python3 &&\
    curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp &&\
    chmod a+x /usr/local/bin/yt-dlp

ENTRYPOINT ["/usr/local/bin/yt-dlp"]
