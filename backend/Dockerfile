FROM python:3.10.1-slim

WORKDIR /app

RUN apt-get update
RUN apt-get install \
    'ffmpeg'\
    'libsm6'\
    'libxext6'  -y


COPY Pipfile* ./
RUN pip install -q --no-cache-dir \
    pipenv===2021.5.29 && \
    pipenv install --system

COPY . .

EXPOSE 8080

CMD ["python", "main.py"]