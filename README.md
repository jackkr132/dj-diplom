# Описание проекта
Проект для работы с интернет магазином. Точнее бэкенд часть интернет магазина!
Данный проект не является идеальным и вы можете доработать этот код! 
Является дипломным проектом по курсу джанго онлайн университета **Нетология!**
Если вас заинтересовал университет пройдите по [ссылке](https://netology.ru/)

## Как работать с проекотом
Для работы с проектом в первую очередь установите независимости и запустите 
миграции(смотрите раздел по установке зависимости). Итак как только установили зависимости можете смело работать с 
проектом и отправить запросы по указанным URL'ам в проекте 
с помощью **Postman** или воспользуйтесь плагином **RestApiClient** в редакторе VSCode или же можете воспользоваться 
панелью админа Django проекта! **Обратите внимания** в тестировании проекта! в настройках settings.py
есть 2 настройки для базы данных! Первая настройке базы данных где настроен СУБД Postgrsql 
должен быть ваш проект а на 2ом случае где настроен SQLite должен быть тестовая база данных! 
Это связана с тем что Django выдаёт ошибку если вы пытаетесь запускать тесты связав их с СУБД Postgresql! 
Поэтому когда тестируете проект либо комментируйте код(c #) и работайте с SQLite(естественно запускаем миграции)
либо сами настройте СУБД по своему усмотрению.

## Необходимые знания для работы с проектом 
* [Python](https://docs.python.org/3/)
* [Django](https://docs.djangoproject.com/en/3.2/)
* [Django-Filter](https://django-filter.readthedocs.io/en/stable/)
* [DjangoRestFramework(DRF)](https://www.django-rest-framework.org/)
* [Pytest-Django](https://pytest-django.readthedocs.io/en/latest/#)
* [Model-Bakery](https://model-bakery.readthedocs.io/en/latest/)

## Устанавливаем зависимости
* наберите команду **pip install -r requirements.txt** в cmd(терминале) проекта чтобы устанавливать
все необходимые требования к проекту
* запустите миграции с помощью команды **python manage.py migrate**
* в проекте есть тестовые данные для быстрой работы с проектом! чтобы передать их в базу данных 
наберите команду **python manage.py loaddata fixtures.json**
* запустите сервер с командой **python manage.py runserver**

## Запуск проекта на Docker 
1. Пишем **docker compose build**
2. **docker compose up**
3. Прогоняем миграции. Для этого сначала наберите **docker exec -it (name_container_for_api) bash**
4. Как только открыли bash консоль пишем **python manage.py migrate**
5. Создаём супер юзера c **python manage.py createsuperuser**
6. Если хотите добавить тестовые данные пишите **python manage.py loaddata fixtures.json**

После этого смело наслаждайтесь сервером)) Удачи в проектах)
