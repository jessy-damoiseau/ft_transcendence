FROM	node:17-alpine3.14

RUN		npm i -g @nestjs/cli

WORKDIR	/app

COPY	./package.json ./
COPY	./package-lock.json ./
COPY	./tsconfig* ./

RUN		npm install --force

COPY	./src ./src
COPY	./upload ./upload
COPY ./templates ./templates

EXPOSE	5000

RUN		npm run build

CMD		nest start