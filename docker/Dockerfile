FROM python:3.10-slim AS backend
WORKDIR /app
COPY app-maker/backend /app/backend
RUN pip install -r /app/backend/requirements.txt

FROM node:18 AS frontend
WORKDIR /app
COPY app-maker/frontend /app/frontend
RUN npm install
RUN npm run build

CMD ["bash"]