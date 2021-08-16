FROM node:14.15-alpine

WORKDIR /usr/src/app/

COPY . .

RUN npm i -g @angular/cli@12.0.0

RUN npm i
RUN ng --version
RUN npm run build

RUN rm -rf /usr/src/app/src
RUN rm -rf /usr/src/app/node_modules

RUN npm install express

EXPOSE $PORT


CMD [ "npm", "run" , "start:prod","start" ]
