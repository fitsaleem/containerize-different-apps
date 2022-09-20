FROM alpine
LABEL maintainer="sr.saleem774@gmail.com"
RUN apk add --update nodejs nodejs-npm
COPY . /src
WORKDIR /src
RUN npm install
ENV CREATEDBY="Saleem Raza"
EXPOSE 8080
ENTRYPOINT ["node", "./app.js"]