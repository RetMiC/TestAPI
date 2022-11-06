# DummyAPI

## Оглавление
1. [Описание проекта](#Описание-проекта)
    1. [POST](#USER)
        1. [GET /user (Get List)](#GET-user-Get-List)
2. [Майнд-карта](#Майнд-карта)


## Описание проекта
https://dummyapi.io/ представляет собой сервис для тестирования АПИ. Для выполнения запросов необходим app-id, который генерируется автоматически при регистрации на сервисе. В качестве тестирования были взят объект **USER**.

### USER
____
#### GET /user (Get List)
Возвращает список пользователей отсортировнных по дате. 
- доступен query params для вывода определенной страницы.
- доступен query params для отображения числа публикаций на странице.

**Response Body**:

**List**
```javascript
{
  data: Array(Model)
  total: number(total items in DB)
  page: number(current page)
  limit: number(number of items on page)
}
```
**Data**
```javascript
{
  id: string(autogenerated)
  text: string(length: 6-50, preview only)
  image: string(url)
  likes: number(init value: 0)
  tags: array(string)
  publishDate: string(autogenerated)
  owner: object(User Preview)
}
```
____
#### POST /post/create (Create Post)
Создает новую публикацию от пользователя. Возвращает данные о публикации.

**Request Body**:



## Майнд-карта
Данная МК представляет собой набор тестов для тестирования объекта **POST**. Подробная проверка расписана для **Get List** и **Create Post**
![Alt-текст](https://i.imgur.com/k4wusSC.png "МК")

Также майнд-карту можно [скачать](https://github.com/RetMiC/DummyAPI/blob/main/POST%20(2).xmind)

## Тест-кейсы
Также были оформлены тест-кейсы в соответствии с майнд-картой.
Тест-кейсы можно посмотреть тут

## Баг-репорты

## Коллекции POSTMAN

## Автотесты

