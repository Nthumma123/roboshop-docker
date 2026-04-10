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
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop 
RUN chown -R roboshop:roboshop /app 
USER roboshop
CMD ["server.js"]
ENTRYPOINT ["node"] 


# FROM node:20
# #USER roboshop
# WORKDIR /app
# COPY package*.json .
# COPY *.js .
# RUN npm install
# ENV REDIS_HOST="redis" \
#     CATALOGUE="catalogue" \
#     CATALOGUE_PORT="8080" 
# CMD ["node","server.js"]



#docker run -d --name redis --network roboshop redis:7 
#docker ps


#docker build -t user:1.0.0 .
#docker images
#docker run -d --name user --network roboshop-network user:1.0
#docker logs -f user
#curl http://localhost:8080/health
#docker exec -it user bash
#docker ps -a

