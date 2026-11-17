# Задание 2: Проектирование REST API для экрана магазинов-партнеров

## 1. Пример REST API запроса
При переходе пользователя на экран со списком магазинов мобильное приложение отправляет GET-запрос на сервер для получения актуального списка.

**HTTP-метод:** `GET`
**URL:** `https://api.petrushka-green.ru/api/v1/stores`

## 2. Пример успешного ответа (JSON)

```json
{
  "stores": [
    {
      "id": 101,
      "name": "METRO",
      "delivery_time_text": "Ближайшая доставка сегодня 21:00-23:00",
      "logo_url": "https://petrushka-green.ru/static/images/metro_logo.png",
      "external_url": "https://online.metro-cc.ru/?ysclid=mwi50pdci642407112"
    },
    {
      "id": 102,
      "name": "Ашан",
      "delivery_time_text": "Ближайшая доставка сегодня 18:00-20:00",
      "logo_url": "https://petrushka-green.ru/static/images/auchan_logo.png",
      "external_url": "https://www.auchan.ru/?utm_referrer=https%3A%2F%2Fyandex.ru%2F"
    },
    {
      "id": 103,
      "name": "ВкусВилл",
      "delivery_time_text": "Быстрая доставка от 20 до 60 минут",
      "logo_url": "https://petrushka-green.ru/static/images/vkusvill_logo.png",
      "external_url": "https://vkusvill.ru/",
      "is_fast_delivery": true
    },
    {
      "id": 104,
      "name": "ВИКТОРИЯ",
      "delivery_time_text": "Ближайшая доставка сегодня 17:00-19:00",
      "logo_url": "https://petrushka-green.ru/static/images/victoria_logo.png",
      "external_url": "https://victoria-group.ru/"
    }
  ]
}
```
## 3. Пояснения к полям

* **`id`** *(integer, обязательное)* — уникальный идентификатор магазина в базе данных.
* **`name`** *(string, обязательное)* — название магазина для отображения на карточке.
* **`delivery_time_text`** *(string, обязательное)* — текстовое описание времени доставки (отображается серым шрифтом).
* **`logo_url`** *(string, обязательное)* — ссылка на изображение логотипа. Мобильное приложение скачивает картинку по этой ссылке.
* **`external_url`** *(string, обязательное)* — ссылка на внешний ресурс. При клике на карточку магазина мобильное приложение открывает эту ссылку.
* **`is_fast_delivery`** *(boolean, опциональное)* — флаг для мобильного приложения. Если `true`, текст доставки выделяется акцентным синим цветом (как у ВкусВилл на макете).

