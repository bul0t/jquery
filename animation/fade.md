# fade
Анимация влияет на: `opacity`.

- fadeIn()
- fadeOut()
- fadeToggle()
- fadeToggle('slow', 0.5) // параметры отвечают за скорость и уровень непрозрачности
- fadeTo('slow', 0.5) // изменяет значение opacity до требуемого значения

Пример:

    const img = $('.img')

    $('.btn--hide').on('click', function() {
        img.fadeOut('slow')
    })

    $('.btn--show').on('click', function() {
        img.fadeIn('slow')
    })

    let i = 0;
    $('.btn--toggle').on('click', function() {
        img.fadeToggle('slow', function() {
            console.log('Анимация закончилась! ' + i++)
        })
    })
