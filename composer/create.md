Создание
==============

## Создание исходников

Для создания стороннего расширения необходимо:
 
* создать репозиторий
* клонировать
* создать файлы `.gitignore` и `composer.json`
* создать папку `src` для исходного кода
* написать код
* отправить изменения в репозиторий

Теперь Вы имеете готовое расширение для подключения его к своему проекту.

Файл `.gitignore` дожен содержать примерно следующее:

```
# phpstorm project files
.idea

# netbeans project files
nbproject
/nbproject/private/

# zend studio for eclipse project files
.buildpath
.project
.settings

# windows thumbnail cache
Thumbs.db

# Mac DS_Store Files
.DS_Store

# local phpunit config
/phpunit.xml
```

Теперь приступим к формированию конфигурации расширения. 
Открываем файл `composer.json` и заполяем его следующими строками:

```json
{
    "name": "example/yii2-extname",
    "type": "yii2-extension",
    "minimum-stability": "dev",
    "autoload": {
        "psr-4": {
             "woop\\extname\\": "src"
         }
    }
}
```

## Загрузка расширения

Чтобы загрузить Ваше расширение в проект, необходимо:

* объявить расширение в файле `composer.json` Вашего проекта
* обновить зависимости `composer update`

Редактируем файл `composer.json` Вашего проекта.

В сегменте `require` добавляем следующее:

```json
"example/yii2-extname": "1.3.*"
```

Если хотите сопровождать пакет:

```json
"example/yii2-extname": "dev-master"
```

При этом вы всегда будете иметь самую свежую версию пакета и сможете комитить и отправлять изменеия.

Если Вы не хотите регистрировать свое расширение в __Composer__, то можно прописать адрес репозитория в сегменте `repositories`:

```json
{
		"type": "git",
		"url": "http://git.example.local/yii2example/yii2-service.git"
}
```
Это указывает, из какого репозитория загружать расширение.

Так же, иногда необходимо отключить безопасный протокол.
В сегменте `config` так:

```json
{
	...,
	"secure-http": false,
	...,
}
```
