FROM node:20
#USER roboshop
WORKDIR /app
COPY package*.json .
COPY *.js .
RUN npm install
ENV REDIS_HOST="redis" \
    CATALOGUE="catalogue" \
    CATALOGUE_PORT="8080" 
CMD ["node","server.js"]



#docker run -d --name redis --network roboshop redis:7 
#docker ps


#docker build -t user:1.0.0 .
#docker images
#docker run -d --name user --network roboshop-network user:1.0
#docker logs -f user
#curl http://localhost:8080/health
#docker exec -it user bash
#docker ps -a

