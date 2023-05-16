
1. Скопируйте проект по ссылке:
   - git@github.com:Pixel2022UA/Homework_10.git

2. Откройте проект в PyCharm и установите необходимые зависимости из файла requirements.txt, используя команду 
   - pip install -r requirements.txt

3. Создайте базу данных выполнив команды:
   - python manage.py makemigrations
   - python manage.py migrate

4. __Скопируйте прикрепленный в LMS Hillel файл .env в корневую директорию проекта (в директорию с фалом manage.py).

5. :exclamation: __В PyCharm убедитесь, что вы находитесь в директории, где расположены файлы проекта и файл manage.py__

6. Запустите RabbitMQ в контейнере Docker используя команду: 
   - docker run -d -p 5672:5672 rabbitmq

7. Запустите Celery worker, используя команду:
    - celery -A exchange_rates worker -l INFO

8. Запустите планировщик задач в Celery(если в этом есть необходимость, т.к. данные на 16.05.2023 существуют):
   - celery -A exchange_rates beat

9. Запустите проект, используя команду:
   - python manage.py runserver

10. Теперь вы можете открыть веб-браузер и перейти на страницу http://127.0.0.1:8000/exchange/