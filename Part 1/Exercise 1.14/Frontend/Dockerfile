FROM node:16

EXPOSE 5000

WORKDIR /usr/src/app
COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm install ./ package.json

RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
