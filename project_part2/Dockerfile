# Dockerfile for book_catalog microservice
FROM python:3.9-slim

WORKDIR /book_catalog

COPY book_catalog/requirements.txt /book_catalog/requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

COPY book_catalog /book_catalog

EXPOSE 8000

ENV DATABASE_URL="postgresql://s223798216_722_week6_user:u83CvgN3n4ZQKnvpL2amBgBVUiMMyGDl@dpg-crbnjfrtq21c73cl3afg-a.oregon-postgres.render.com/s223798216_722_week6"

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
