FROM python:3.9-slim
WORKDIR /app

# install deps first (cache-friendly)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# copy source
COPY . .

EXPOSE 8080

CMD ["python","-m","uvicorn","app.main:app","--host","0.0.0.0","--port","8080"]
