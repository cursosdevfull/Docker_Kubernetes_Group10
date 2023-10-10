FROM node:alpine3.18 as BUILDER

ARG DIR

WORKDIR /build

COPY ${DIR}/package.json .

RUN npm install

COPY ${DIR}/. .

RUN npm run build --prod

FROM nginx:alpine

COPY --from=BUILDER /build/dist/app-courses /usr/share/nginx/html

COPY conf/default.conf /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]