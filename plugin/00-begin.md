# Пишем плагин правильно
Пишем jQuery плагин правильно:
- добавляем плагин в библиотеку jQuery `$`
- возвращаем `this` (для возможноти использования цепочки вызовов)

Код плагина (помещаем его в файл `pColor.js`, подключаем после jQuery):

    (function($) {
        $.fn.pColor = function() {
            $(this).on('click', function(){
                $(this).css('color', '#ff0000');
            })
            return this;
        };
    })(jQuery);

Код использования плагина (помещаем в `common.js`):

    $('p').pColor() // кликаем по абзацам, они становятся красными
