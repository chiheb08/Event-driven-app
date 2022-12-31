FROM python:3.9.7-slim
RUN pip install -U pip
RUN pip install pipenv
WORKDIR /app
COPY [ "Pipfile", "Pipfile.lock", "./" ]
RUN pipenv install --system --deploy
COPY [ "email_backend.py", "./" ]
EXPOSE 5002
ENTRYPOINT ["python", "email_backend.py"]