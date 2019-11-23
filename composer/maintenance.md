Сопровождение
===
## Перенос функционала

При переносе функционала, в док-блок добавляем параметр `@deprecated` и указываем куда именно переместили функционал.

Например:

```php
/**
 * Class Db
 *
 * @package yii2rails\app\helpers
 *
 * @deprecated moved to \yii2rails\app\domain\helpers\Db
 */
class Db extends \yii2rails\app\domain\helpers\Db {}
```

## Зависимости

Указываем зависимости от других пакетов в `composer.json` 