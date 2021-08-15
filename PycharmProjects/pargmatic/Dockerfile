FROM python:3.9.0

WORKDIR /home/

RUN echo "testing1234"

RUN git clone https://github.com/gwakseunghui/seunghui_study.git

WORKDIR /home/seunghui_study/PycharmProjects/pargmatic/

RUN pip install -r requirements.txt

RUN pip install gunicorn

RUN pip install mysqlclient

EXPOSE 8000

CMD ["bash", "-c", "python manage.py collectstatic --noinput --settings=pargmatic.settings.deploy && python manage.py migrate --settings=pargmatic.settings.deploy && gunicorn pargmatic.wsgi --env DJANGO_SETTINGS_MODULE=pargmatic.settings.deploy --bind 0.0.0.0:8000"]