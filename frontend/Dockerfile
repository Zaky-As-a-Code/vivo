FROM node:13.8.0 AS Build
ENV  API_URL=http://backendsvc:3030

WORKDIR  /vivo/frontend
COPY . .
RUN git clone https://github.com/Zaky-As-a-Code/vivo.git
#RUN npm install
#RUN npm run build


FROM nginx:latest
WORKDIR /usr/share/nginx/html
COPY --from=Build vivo/frontend/* .


