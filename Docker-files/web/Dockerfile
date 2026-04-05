from nginx:latest
LABEL "Project"='Vprofile'
LABEL "Author"="Vishnu"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf

CMD ["sh", "-c", "sleep 10 && nginx -g 'daemon off;'"]
