# CI: taskflow-infra
FROM node:24-slim

WORKDIR /app

COPY backend/package*.json ./backend/
RUN cd backend && npm install --omit=dev

COPY backend/server.js ./backend/server.js
COPY backend/db.js ./backend/db.js
COPY frontend ./frontend
COPY migrations ./migrations

WORKDIR /app/backend

EXPOSE 3000

CMD ["node", "server.js"]
