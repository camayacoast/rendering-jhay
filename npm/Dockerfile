FROM node:12.16.2

# ARG UID
# ARG GID

# ENV UID=${UID}
# ENV GID=${GID}

RUN mkdir -p /var/www/html

WORKDIR /var/www/html

#ADD ./web-app/master .

# MacOS staff group's gid is 20, so is the dialout group in alpine linux. We're not using it, let's just remove it.
# RUN delgroup dialout

# RUN addgroup -g ${GID} --system nodeuser
# RUN adduser -G nodeuser --system -D -s /bin/sh -u ${UID} nodeuser

RUN npm install --include=dev

CMD ["npm", "start"]