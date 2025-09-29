FROM almalinux:9
RUN dnf install nginx -y
LABEL author="vishnu" \
      course="docker"
EXPOSE 80
RUN rm -rf /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html/index.html
WORKDIR /usr/share/nginx
ARG name
ARG age
RUN echo "hi i am ${name} age is ${age}"
CMD [ "nginx", "-g", "daemon off;" ]


# CMD [ "ping", "-c5", "google.com" ]
# CMD [ "google.com" ]
# ENTRYPOINT [ "ping", "-c6" ]
