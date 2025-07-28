FROM node:18-alpine

WORKDIR /app
COPY package.json yarn.lock ./
RUN yarn install

COPY . .

RUN yarn build

# Serve with a static server
RUN yarn global add serve
CMD ["serve", "-s", "build"]
EXPOSE 3000
