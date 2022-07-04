![example workflow](https://github.com/hulkluck/foodgram-project-react/actions/workflows/main.yml/badge.svg)

### Описание проекта Foodgram:

Вы можете создавать рецепты, добавлять их в избранное и в корзину для покупок. Из корзины есть возможность выгрузить .txt файл
с необходимыми ингредиентами, чтобы приготовить понравившееся блюдо.
Также, вы можете подписываться на понравившихся вам авторов рецептов.
Без регистрации вам доступно чтение рецептов.

Проект реализован через RESTful API (включая Django и Django REST Framework).

Поддерживает методы GET, POST, PUT, PATCH, DELETE

Предоставляет данные в формате JSON

### Как запустить проект:

Для начала убедитесь, что у вас установлен Docker командой:

```
* docker -v
```

Клонируйте репозиторий и перейдите в него в командной строке:

```
* https://github.com/hulkluck/foodgram-project-react

```

Перейдите в папку с проектом и создайте и активируйте виртуальное окружение:

```
* cd foodgram-project-react
* python3 -m venv env
```

```
* source venv/Scripts/activate
```

```
* python3 -m pip install --upgrade pip
```

Установите зависимости из файла requirements.txt:

```
* pip install -r requirements.txt
```

Перейдите в папку с файлом docker-compose.yaml:

```
* cd infra
```

Разверните контейнеры:

```
* docker-compose up -d --build
```

Выполните миграции, создайте суперпользователя, соберите статику:

```
* docker-compose exec backend python manage.py migrate
* docker-compose exec backend python manage.py createsuperuser
* docker-compose exec backend python manage.py collectstatic --no-input
```


Создайте дамп (резервную копию) базы:

```
* docker-compose exec backend python manage.py dumpdata > fixtures.json
```

## Приложение работает по ссылкам:
* http://51.250.109.244/admin/
* http://51.250.109.244/recipes


### Автор проекта Foodgram:
* Бек Антон
* https://github.com/hulkluck/


### License
* MIT @ Anton Bek
