FROM node:8.4.0-alpine AS build

ADD src /opt/src
ADD public /opt/public
ADD package.json /opt/package.json

WORKDIR /opt

RUN yarn install
RUN yarn build

FROM node:8.4.0-alpine

RUN yarn global add serve

COPY --from=build /opt/build /opt

WORKDIR /opt

EXPOSE 5000

CMD ["serve", "-s ."]




