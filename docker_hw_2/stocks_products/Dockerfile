FROM python:3.10-alpine

WORKDIR /src

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

RUN pip install --upgrade pip

COPY ./requirements.txt .
RUN pip install -r /src/requirements.txt 

COPY . /src

EXPOSE 8000
ENV MY_ENV=netology


#CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]

