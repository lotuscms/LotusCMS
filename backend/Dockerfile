FROM node:12
ARG NODE_ENV=production
ENV NODE_ENV=${NODE_ENV}
RUN mkdir /app
WORKDIR /app
RUN git clone https://github.com/lotuscms/LotusBackend.git .
RUN git checkout -b AzerothCore
RUN git pull origin AzerothCore
RUN yarn
COPY conf.template.json /app/conf.json
CMD ["yarn", "start-prod"]
