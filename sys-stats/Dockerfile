FROM node:latest as build
RUN mkdir /app
WORKDIR /app
COPY . /app
RUN npm install
RUN npm update
RUN npm run build
CMD ["npm" , "start"]

FROM nginx:latest
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]