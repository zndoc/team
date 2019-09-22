```php
<?php
# между констркуцией <?php и namespace один отступ (комменты учитываются)
namespace App\Rules;
# один отступ
# class/trait/interface (фигурные скобки с переносом на новую строку)
# свойства класс описываются минимально подробно:
/**
 * Класс для описания стиля кода
 *
 * @property integer $style тип стиля кода разраба
 * @property string $level уровень разраба
 *
 * @author kamaelkz <kamaelkz@yandex.kz>
 */
class App
{
    /**
     * @var integer
     */
    public $style;

    /**
     * @var string
     */
    public $level = 1;

    /**
     * # минимально описываем что делает метод
     * # типы входных параметров @param
     * # результат выполнения @return
     * # фигурная скобка метода с переносом на новую строку
     * # исключения @throws
     *
     * Проверка стиля разработчика
     *
     * @param string $a
     * @param string $b
     * @param string $c
     *
     * @return boolean
     */
    public function checkStyle(string $a, string $b, string $c)
    {
        #визуальное разделение отрицания от переменной пробелом
        if(! $a) {
            return false;
        }
        #если условие большое (внимание на разделение и пробелы в конструкции)
        #если функция имеет большое кол-во условных операторов, комментируем конструкции
        #это поможет новым людямв проекте и Вам после перекура
        if(
            ! $a
            || ! $b
            || ! $c
        ) {
            return false;
        }
        # хорошим тоном является ренний выход из фунуции
        # что то нас не устраивает делаем return
        # избегаем логики в условных оператарах
        if($a == 'don\'t do that') {
            #......
        }
        #альтернатива
        if($a !== 'don\'t do that') {
            return false;
        }
        #между констуркциями перенос строки (есть место для коммента + читабельно)
        # это касается многих конструкций switch/ try и тд
        if($b !== 'don\'t do that') {
            return false;
        }

        if($с == 'don\'t do that') {
            return false;
        }

        try {
            #объеденение строк пробел до и после точки, оператора concat
            $result = $a . $b . $c;
            $result = "{$a}{$b}{$c}";
        } catch (\Exception $e) {
            return false;
        }
        #return метода разделяется переносом строки
        $this->level = 'master';
        
        return $result;
    }
}
#закрыл красавчик
?>
```

