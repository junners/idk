FROM node:alpine AS build
ENV NODE_ENV=production

WORKDIR /opt/idk
COPY . .

RUN npm install --production
RUN npm run build

USER idk

FROM build as hosting

RUN npm start