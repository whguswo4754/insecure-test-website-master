FROM node:21.2-alpine3.18

ENV PROJECT_URL="https://github.com/camcamfresh/insecure-test-website/archive/master.zip"

RUN apk add busybox wget unzip && \
	wget -qO- $PROJECT_URL | busybox unzip - && \
	cd insecure-test-website-master && \
	npm install && \
	npm run build && \
	npm install express

CMD ["node", "insecure-test-website-master/server.js"]
