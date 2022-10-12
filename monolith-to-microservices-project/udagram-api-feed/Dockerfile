# FROM node:18-alpine3.15
# COPY . .
# RUN npm install .
# RUN npm run build
# EXPOSE 8080
# CMD [ "npm","run"," prod" ] 

FROM node:18-alpine3.15

ENV POSTGRES_USERNAME=postgres 
ENV POSTGRES_PASSWORD=postgres 
ENV POSTGRES_HOST=localhost
ENV POSTGRES_DB=postgres 
ENV AWS_BUCKET=s3://udagram-716928399409-dev/udagram/ 
ENV AWS_REGION=us-east-1 
ENV AWS_PROFILE=default 
ENV JWT_SECRET=testing 
ENV URL=http://localhost:8100

WORKDIR /usr
COPY package.json ./
COPY tsconfig.json ./
COPY src ./src
RUN npm install
EXPOSE 8080
CMD [ "npm","run","dev" ] 
