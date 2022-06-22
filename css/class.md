# Классы
Работаем с классами в CSS.

Добавляем класс элементу:

    $(".wrap").addClass("wrap--mod");

Используем функцию для выборки:

    $("li").addClass(function(i){
        if(i == 2) return 'title--mod';
    })

Проверяем имеет ли элемент данный класс:

    $('h1').hasClass('title')

Удаляем класс:
    
    $('h1').removeClass('title')

    $("li").removeClass(function(i){
        if(i == 2) return 'title--mod'
    })

Переключаем класс (проверяем по событию):

    $('h1').toggleClass('title')

Изучить дополнительно:

    toggleClass(className, switch)
    toggleClass(function(index, currentClass, switch){ return className }, switch)

## Разное
- добавлять удалять и т.д, можно сразу несколько классов `addClass("title title--mod")`
