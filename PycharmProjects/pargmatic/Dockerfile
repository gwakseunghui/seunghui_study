FROM python:3.9.0

WORKDIR /home/

RUN git clone https://github.com/gwakseunghui/seunghui_study.git

WORKDIR /home/seunghui_study/PycharmProjects/pargmatic/

RUN pip install -r requirements.txt

RUN echo "SECRET_KEY=django-insecure-epgw9f#btvaljvukfhi(o4)-@(-5ka!pxe*9288k%$-r+how*v" > .env

RUN python manage.py migrate

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]