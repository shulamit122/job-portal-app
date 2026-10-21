FROM node:22-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci --omit=dev

COPY index.js ./
COPY controllers ./controllers
COPY middlewares ./middlewares
COPY models ./models
COPY routes ./routes
COPY utils ./utils

ENV NODE_ENV=production
EXPOSE 3000

CMD ["node", "index.js"]