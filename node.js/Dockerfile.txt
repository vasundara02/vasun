FROM node:14
WORKDIR /usr/src/app
COPY package *. json./
RUN ppm install
COPY . .
EXPOSE 3000
CMD["node","App.js"]