FROM node:alpine as builder

WORKDIR /usr/local/app

COPY ./ /usr/local/app/

RUN npm install

RUN npm run build

FROM nginx:alpine

COPY --from=builder /usr/local/app/dist/angular-starter /usr/share/nginx/html

EXPOSE 80
