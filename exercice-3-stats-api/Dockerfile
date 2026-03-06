FROM python:3.12-slim AS builder

WORKDIR /build

COPY requirements.txt .

RUN pip install --upgrade pip \
    && pip install --prefix=/install -r requirements.txt

COPY . .

FROM python:3.12-alpine 

WORKDIR /app

COPY --from=builder /install /usr/local

COPY . .

EXPOSE 4000

CMD ["python", "app.py"]