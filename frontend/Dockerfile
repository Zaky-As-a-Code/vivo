FROM node:13.8.0 AS Build
ENV  API_URL=http://backendsvc:3030
RUN git clone https://github.com/devops-user22/DevOps-proj.git
WORKDIR  /vivo/frontend
#RUN npm install
#RUN npm run build
COPY dist .

FROM nginx
WORKDIR /usr/share/nginx/html
COPY --from=Build vivo/frontend/dist .



