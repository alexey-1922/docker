FROM python:3.8

WORKDIR /dj_app

COPY ./dj_app /dj_app

RUN pip install -r /dj_app/requirements.txt

ENV SECRET_KEY fgfyyrtrjtmtyiyi364757AASSDFDFFGF
ENV DEBUG 1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]
