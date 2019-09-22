Пагинация
===

Инфо о пагинации отправляется в виде GET-параметров `page`, `per-page`, `offset`.

## GET-параметры

### page

Текущая страница

```json
{
		"page": 3,
}
```

### per-page

Количество сущностей на каждой странице

```json
{
		"per-page": 15,
}
```

### offset

Смещение выборки

```json
{
		"offset": 15,
}
```

Начнет выборку 15-той сущности. Это может быть полезно для *Lazy load*.

## Получаемые заголовки

* X-Pagination-Total-Count - Количество всех сущностей
* X-Pagination-Page-Count - Количество страниц
* X-Pagination-Per-Page - Количество сущностей на страницу
* X-Pagination-Current-Page - Текущая страница
* X-Pagination-Offset - Смещение
