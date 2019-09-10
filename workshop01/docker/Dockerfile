FROM node:latest
ENV DB_HOST=mydb
ENV DB_PORT=3306
ENV APP_PORT=3000
ENV APP_DIR=/app

WORKDIR ${APP_DIR}

ADD main.js .
ADD package-lock.json .
ADD package.json .
ADD config config
ADD public public
ADD views views

RUN npm install
EXPOSE ${APP_PORT}


#start app

ENTRYPOINT [ "node", "main.js" ]
