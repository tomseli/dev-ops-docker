FROM python:3.13-alpine

EXPOSE 8000

WORKDIR /usr/src/app

RUN pip install mkdocs

COPY . .

ENTRYPOINT [ "mkdocs", "serve", "--dev-addr=0.0.0.0:8000"]