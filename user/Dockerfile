FROM node:20
#USER roboshop
WORKDIR /app
COPY package*.json .
COPY *.js .
RUN npm install
ENV MONGO = "true" \
    MONGO_URL = "mongodb://mongodb:27017/catalogue" \
    REDIS_URL="redis://redis:6379"
CMD ["node","server.js"]

#docker build -t user:1.0.0 .
#docker images


#docker build -t user:1.0.0 .
#docker run -d --name user --network roboshop user:1.0.0
#docker ps
#docker logs -f user


#curl http://localhost:8080/health
#docker exec -it user bash
#docker ps -a
