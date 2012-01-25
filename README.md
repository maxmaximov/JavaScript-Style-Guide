Стандарты кодирования JavaScript
================================

Кодировка
---------

UTF-8 (простой, без сигнатуры Byte Order Mark, BOM).

Символ перевода строки
----------------------

LF, он же 0x0A, он же U+000A, он же UNIX.

Отступы и блоки
---------------

* Стиль: 1TBS
http://en.wikipedia.org/wiki/Indent_style#Variant:_1TBS.

* Ширина отступа: 4 пробела (символ табуляции не используем).

``` javascript
if (x < 0) {
    puts("Negative");
    negative(x);
} else {
    puts("Non-negative");
    nonnegative(x);
}
```

Пробелы
-------

* Операторы отделяются одним пробелом.
* Аргументы функции отделяются друг от друга одним пробелом. Ведущий и замыкающий пробел не используются.

Именование идентификаторов (переменных, «констант», функций, «классов», свойств, методов)
-----------------------------------------------------------------------------------------

* Стиль: CamelCase
http://en.wikipedia.org/wiki/CamelCase#Current_usage_in_computing.

``` javascript
var testVariable = true;
 
function doSomeDirtyStuff (firstParam, secondParam) {
};
```

* Имена классов: с большой буквы.

* Имена функций (методов) и переменных (свойств): с маленькой буквы.

* «Приватные» методы и свойства: префикс «_».

``` javascript
var sidebar = new Sidebar();
var instanceOfMyClass = new MyClass();

var object = {
    _privateProperty: null,
    _privateFunction: function (param) {
        this._privateProperty = param;
    }
};
```

Ширина строки
-------------

*Ограничивать?*

Стиль комментариев
------------------

*Описа́ть.*

Отладка
-------

Отладочные сообщения alert-ами — зло. Везде, где это возможно, пользуемся специальным инструментарием:
* Logger.log().
* console.log() (там, где App не используется).

Ненавязчивый JavaScript
-----------------------

Инлайновые скрипты использовать запрещено.

Ссылки
------

http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
http://docs.jquery.com/JQuery_Core_Style_Guidelines
