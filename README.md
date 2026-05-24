# Flask Application with PostgreSQL, Redis & Nginx

## Описание проекта

Веб-приложение на Flask

## Технологический стек

- **Flask 2.3** - веб-фреймворк на Python
- **PostgreSQL 15** - реляционная база данных
- **Redis 7** - кэширование
- **Nginx Alpine** - reverse-proxy сервер
- **Docker Compose** - оркестрация контейнеров

## Функциональность

### Эндпоинты API

- `GET /` - Главная HTML-страница с отображением имени приложения
- `GET /visits` - JSON со счетчиком посещений и статусом кэширования
- `GET /health` - JSON со статусом подключения к БД и Redis

### Особенности

- Счетчик посещений сохраняется в PostgreSQL
- Redis кэширует значение счетчика на 10 секунд
- Nginx выступает в роли reverse-proxy
- Две изолированные сети: frontend и backend
- Healthcheck для всех сервисов

## Требования

- Docker Engine 20.10+
- Docker Compose 2.0+

## Инструкция по запуску

### 1. Клонирование репозитория

```bash
git clone <ссылка_на_репозиторий>
cd variant-2