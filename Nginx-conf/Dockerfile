FROM node:alpine as builder
WORKDIR '/usr/src/app'
COPY packaage.json .
RUN npm install
COPY ./ ./

# 밑이 운영 서버 빌드 run stage 
FROM nginx
COPY --from=builder /usr/src/app/build /usr/share/nginx/htmp
