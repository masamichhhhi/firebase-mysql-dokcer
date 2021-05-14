FROM node:12

RUN apt-get update && \
  npm install -g firebase-tools


WORKDIR /app/functions

# COPY package.json ./

CMD npm install \
  && firebase use ${FIREBASE_PROJECT} --token ${FIREBASE_TOKEN} \
  && npm run serve


EXPOSE 4000 5000 5001