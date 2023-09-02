# Kittygram 🐱

## Описание проекта ✏️

Социальная сеть для обмена фотографиями любимых котиков! На сайте возможна регистрация новых пользователей, загрузка фото своих пушистых питомцев, просмотр фото других пользователей. Также имеется возможность присваивать имена, цвет, достижения и год рождения котейкам.

## Технологии 🛠️

- Python 3.9
- Django==3.2.3
- Nginx
- Gunicorn
- Nginx
- Certbot
- Docker
- GitHub Actions

### Запуск проекта 🌐
1. Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:vovan46rus/kittygram_final.git
cd kittygram_final
```
2. В корне проекта создать файл .env и добавить в него свои данные.
Пример:
```
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
```
3. Запустить проект через docker-compose:
```
docker compose -f docker-compose.yml up
```
4. Выполнить миграции:
```
docker compose -f docker-compose.yml exec backend python manage.py migrate
```
5. Создать суперюзера:
```
sudo docker compose -f docker-compose.yml exec backend python manage.py createsuperuser
```
6. Собрать статику и скопировать ее:
```
docker compose -f docker-compose.yml exec backend python manage.py collectstatic
docker compose -f docker-compose.yml exec backend cp -r /app/static_backend/. /backend_static/static/
```
### Автор 👨‍💻
[Владимир Коваленко](https://github.com/vovan46rus)

### Cвязь 📡
[Телеграм](https://t.me/icq609258000)
