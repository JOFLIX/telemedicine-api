# Информация о запросах на консультации

## Поиск по консультациям

`GET /api/v1/request/get-all` вернёт список консультаций.

### Запрос

Имя | Тип | Описание
--- | --- | ---
ids | array | уникальные идентификаторы консультации вида текстовая консультация
statuses | array | статусы консультации
hasMedicalReport | boolean | наличие медицинского заключения
order | string | сортировать по полю (Created, Status)
asc | boolean | сортировать по возрастанию
limit | integer | максимальное кол-во записей в ответе
offset | integer | смещение (сколько записей пропустить)

### Ответ

[Объект Запрос на консультацию](./contracts.md#Consultation-Request)

```json
{
  "items": [
    {
      //.. объект запрос на консультацию
    }
  ],
  "count": 10,
  "totalCount": 15
}
```

## Медицинские заключения

`GET /api/v1/request/medical-report` вернёт медицинское заключение для указанной консультации.

### Запрос

Имя | Тип | Описание
--- | --- | ---
id | string | уникальный идентификатор консультации

### Ответ

[Объект Медицинское заключение](./contracts.md#Medical-Report)

```json
{
  //.. объект медицинское заключение
}
```

## Загрузка и прикрепление документа к запросам на консультации

`POST /api/v1/request/attach-document` вернёт информацию о прикрепленном к запросу на консультацию медиа-объекте.

### Запрос

Имя | Тип | Описание
--- | --- | ---
binary | string | multipart/form-data содержимое файла
requestId | string | ID запроса на консультацию

### Ответ

[Объект Медиа](./contracts.md#Media)

```json
{
  //.. объект медиа
}
```