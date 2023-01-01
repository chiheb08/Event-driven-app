FROM python:3.9.7-slim
RUN pip install -U pip
RUN pip install pipenv
WORKDIR /app
COPY [ "Pipfile", "Pipfile.lock", "./" ]
RUN pipenv install --system --deploy
COPY [ "analytics_backend.py", "./" ]
ENTRYPOINT ["python", "analytics_backend.py"]