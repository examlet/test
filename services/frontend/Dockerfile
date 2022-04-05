FROM node:lts as builder

WORKDIR /app-builder

COPY package.json .

RUN yarn install

COPY . .

RUN npm run build


# # #

FROM node:lts

WORKDIR /app

COPY package.json ./

COPY --from=builder /app-builder/.output ./.output

ENV PORT 3000
ENV HOST 0.0.0.0

EXPOSE $PORT

CMD ["yarn", "start"]