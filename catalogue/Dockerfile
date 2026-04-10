FROM node:20.20.2-alpine3.23 as builder
WORKDIR /app
COPY package*.json .
COPY *.js .
RUN npm install

# code + node_modules 

FROM node:20.20.2-alpine3.23
WORKDIR /app
EXPOSE 8080
COPY --from=builder /app /app
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue" \
    REDIS_URL="redis://redis:6379"
CMD ["node","server.js"]








# FROM node:20
# #USER roboshop
# WORKDIR /app
# COPY package.json .
# COPY *.js .
# RUN npm install
# ENV MONGO="true" \
#     MONGO_URL="mongodb://mongodb:27017/catalogue"
# CMD ["node","server.js"]

#docker build -t catalogue:1.0.0 .
#docker images
#docker run -d --name catalogue --network roboshop-network catalogue:1.0.0

#docker exec -it catalogue bash



#curl http://localhost:8080/health

#docker logs -f catalogue