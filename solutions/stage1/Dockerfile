FROM python:3.7-slim

WORKDIR /app
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apt-get update -y && apt-get upgrade -y && apt-get install -y ffmpeg libsm6 libxext6 libglib2.0-0
COPY requirements.txt .
RUN pip3 install -r requirements.txt
EXPOSE 5000
COPY OCR_routes.py app.py
CMD ["flask", "run"]