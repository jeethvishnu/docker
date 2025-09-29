FROM node:20-alpine  as build
RUN adduser -D expense
ENV DB_HOST=mysql
RUN mkdir /app
RUN chown expense:expense -R /app
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install


FROM node:20-alpine 

ENV DB_HOST=mysql
RUN adduser -D expense
WORKDIR /app
COPY --from=build /app ./
USER expense

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
