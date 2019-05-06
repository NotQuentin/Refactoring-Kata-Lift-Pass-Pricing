FROM node:10.15-alpine


WORKDIR /home/node/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY ./package*.json ./

RUN rm -rf /home/node/app/node_modules
RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

USER node
RUN npm install
RUN ls -la /home/node/app/node_modules

USER root
COPY --chown=node:node . .

# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
#COPY . .

EXPOSE 5010
USER node
CMD [ "npm", "start" ]