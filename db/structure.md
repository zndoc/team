# Структура БД

Есть два варианта структуры БД:

* **плоская** БД, где все таблицы находятся в одной схеме
* БД, **разбитая на схемы**

## Плоская БД

Для плоской БД, таблицы именуем, начиная с префикса предметной области.

Пример именования таблиц из предметных областей (пользователь, файловое хранилище, справочники):

* user_account
* user_role_assignment
* user_person
* storage_file
* storage_image
* storage_service
* storage_service_thumb
* reference_item
* reference_book
* reference_item_localization
* reference_book_localization

## БД со схемами

Для варианта с разбитием на схемы, каждую предметную область помещаем в отдельную схему.

Например:

* таблицы предметной области "пользователь", храним в схеме "user"
* таблицы предметной области "файловое хранилище", храним в схеме "storage"
* таблицы предметной области "справочники", храним в схеме "reference"

Вот что примерно должно получиться:

* user
	* account
	* role_assignment
	* person
* storage
	* file
	* image
	* service
	* service_thumb
* reference
	* item
	* book
	* item_localization
	* book_localization

> Note: Если БД позволяет использовать схемы, то разбивка по схемам более предпочтительна.
