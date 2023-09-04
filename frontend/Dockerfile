FROM node:13.8.0 AS Build
ENV  API_URL=http://backend:3030
RUN git clone https://github.com/Zaky-As-a-Code/vivo.git
WORKDIR  /vivo/frontend
RUN npm install
RUN npm run build

FROM nginx
WORKDIR /usr/share/nginx/html
COPY --from=Build vivo/frontend/dist .
