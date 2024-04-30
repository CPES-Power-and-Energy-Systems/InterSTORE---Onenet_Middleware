FROM eurodynrnd/sofia-frontend:latest

ARG BACKEND_URL

COPY empty.png /usr/share/nginx/html/assets/img/logo_ed.png
COPY empty2.png /usr/share/nginx/html/assets/img/logo-H2020.png
COPY background.jpg /usr/share/nginx/html/assets/img/bg/dark-material-bg.jpg

RUN sed -i 's/, European Dynamics/, Onenet Application/g' /usr/share/nginx/html/main.*.js
RUN touch /usr/share/nginx/html/assets/config.js
RUN echo "window['backend_url'] = '"${BACKEND_URL}"'; window['backend_on_proxy_path'] = '';" >> /usr/share/nginx/html/assets/config.js
