FROM node:20
RUN useradd expense
ENV DB_HOST=mysql
RUN mkdir /app
RUN chown expense:expense -R /app
WORKDIR /app
COPY package.json .
COPY  TransactionService.js .
COPY *.js .
RUN npm install
CMD [ "node", "index.js" ]








# FROM node:20
# RUN useradd expense
# ENV DB_HOST=mysql
# RUN mkdir /app
# RUN chown expense:expense -R /app
# WORKDIR /app
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD [ "node", "index.js" ]
