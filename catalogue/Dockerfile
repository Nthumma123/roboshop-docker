FROM node:20
USER roboshop
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO = "true" \
    MONGO_URL = "mongodb://mongodb:27017/catalogue"
CMD ["node","server.js"]

#docker build -t catalogue:1.0.0 .
#docker images
#docker run -d --name catalogue --network roboshop-network catalogue:1.0.0

#docker exce -it catalaogue bash



#curl http://localhost:8080/health

#docker logs -f catalogue