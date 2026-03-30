FROM nginx:1.24.0
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf  /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf
COPY static /usr/share/nginx/html


#docker build -t frontend:1.0.0 .
#docker images
#docker run -d --name frontend --network roboshop -p 80:80 frontend:1.0.0
#docker logs -f frontend
#curl http://localhost/health
#docker exec -it frontend bash
#docker ps -a


#cd /etc/nginx/conf.d
#cat default.conf
 #ANY chnages in image configuraation - rebuild it 