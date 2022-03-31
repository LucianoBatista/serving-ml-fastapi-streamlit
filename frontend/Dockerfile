FROM python:3.10.1-slim

WORKDIR /app

COPY Pipfile* ./
RUN pip install -q --no-cache-dir \
    pipenv===2021.5.29 && \
    pipenv install --system

COPY . .

EXPOSE 8501

CMD ["streamlit", "run", "main.py"]