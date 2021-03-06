# Медицинская карта

## Получение информации о медицинской карте пациента

`GET /api/v1/medicalcard/get/{id}` вернёт информацию о медицинской карте пациента.

### Запрос

Имя | Тип | Описание
--- | --- | ---
id | string | уникальный идентификатор пациента

### Ответ:

[Объект Медицинская карта](./contracts.md#medical-card)

```json
{
  //.. объект медицинская карта
}
```

## Выдача доступа врачу к медицинской карте

`POST /api/v1/medicalcard/share` вернёт информацию о медицинской карте пациента.

### Запрос

Имя | Тип | Описание
--- | --- | ---
doctorId | integer | уникальный идентификатор доктора
expiredAtUtc | datetime | дата окончания доступа врача к мед. карте

### Ответ:

[Объект Медицинская карта](./contracts.md#medical-card)

```json
{
  //.. объект медицинская карта
}
```
