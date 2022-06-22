# Оптимизация

## Делегирование событий
Вешаем обработчик на все ячейки таблицы:

    $("table td").on("click", function() { 
        /* ... */
    });

Тоже самое, но более оптимизированный вариант:

    $("table").on("click", "td", function() { 
        /* ... */
    });

Записываем все клики пользователя по элементам страницы, внутри тега body:

    $("body").on("click", "*", function() {
        console.info("Click on " + this.tagName);
    });