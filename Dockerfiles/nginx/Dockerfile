FROM nginx 
LABEL "Project" = "Docker-Local"
LABEL "Author" = "MSaqibBhatti"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf