FROM node:19-alpine as build
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
ARG REACT_APP_BACKEND_HOST="http://a2d713ccba98d471583fbcd747cd19d3-723770991.eu-west-2.elb.amazonaws.com:3000"
ENV REACT_APP_BACKEND_HOST=$REACT_APP_BACKEND_HOST
RUN npm run build

FROM nginx:alpine
COPY --from=build /app/dist /usr/share/nginx/html