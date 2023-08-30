FROM python:3.10

COPY . /exercise_2

COPY ./requirements.txt /exercise_2/requirements.txt
RUN pip3 install --no-cache-dir --upgrade -r /exercise_2/requirements.txt 

EXPOSE 7070
WORKDIR exercise_2

RUN python manage.py migrate
RUN python manage.py collectstatic --noinput 

CMD ["gunicorn", "--bind", "0.0.0.0:7070", "--workers", "3", "stocks_products.wsgi:application"]