# ENF — Django E-commerce

Минималистичный интернет-магазин, вдохновлённый эстетикой Enfants Riches Déprimés.

Проект построен на **Django + HTMX + Alpine.js** и включает полноценный e-commerce функционал:

- каталог товаров
- корзину
- регистрацию и профиль пользователей
- оформление заказов
- онлайн-оплату
- деплой через Docker

---

# Технологии

## Backend
- Django
- Python
- PostgreSQL
- Gunicorn

## Frontend
- HTMX
- Alpine.js

## Infrastructure
- Docker
- Nginx

## Payments
- Stripe

---

# Возможности

- Каталог товаров
- Страница товара
- Корзина
- Регистрация и логин
- Профиль пользователя
- Оформление заказа
- Онлайн-оплата
- Админка Django
- Docker деплой
- Production конфигурация с Nginx

---

# Архитектура проекта

```
enf/
├ main        # каталог и товары
├ cart        # корзина
├ users       # регистрация / профиль
├ orders      # оформление заказов
├ payment     # stripe + crypto
└ enf         # настройки проекта
```

---

# Установка и запуск

## Клонировать репозиторий

```bash
git clone https://github.com/MarattYa/enf.git
cd enf
```

---


## Заменить файл `.env.example` на `.env`

```
POSTGRES_DB=enf
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres

SECRET_KEY=change_me
DEBUG=True

STRIPE_SECRET_KEY=
STRIPE_PUBLIC_KEY=
```

---

## Запустить контейнеры

```bash
docker compose up --build
```

После запуска проект будет доступен:

```
http://localhost
```

---

# Основные зависимости

```
Django
psycopg2
stripe
gunicorn
python-dotenv
pillow
requests
```

---

# Приложения

## main
Каталог товаров  
Карточки товаров  
Категории

## cart
Корзина пользователя  
HTMX обновления

## users
Регистрация  
Авторизация  
Профиль

## orders
Создание заказа  
История заказов

## payment
Stripe оплата  

---

# Development

Установка зависимостей:

```bash
pip install -r requirements.txt
```

Миграции:

```bash
python manage.py migrate
```

Запуск:

```bash
python manage.py runserver
```

---


# Roadmap

- Избранные товары
- Отзывы
- Админ панель для заказов
- Email уведомления
- API
