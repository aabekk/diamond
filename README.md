# diamond
Использовались технологии: `pug, sass, gulp, БЭМ`
### Задача
 - [X] Создать счетчик с бесконченым циклом и задержкой последнего значения без применения `JS` _(обязательное условие)_
 - [X] Менять пропорционально размер _текста_ и элемента в зависимости от размеров экрана
 - [X] Сделать так, чтобы при _наведении_ на этот элемент, менялся задний фон
### Решение задачи
+ Счетчик обрабатывается с помощью задержки анимации _`animation-delay`_
+ К тексту применяем _`vh`_. Элемент изменяется пропорционально с помощью дополнительно элемента c _внешним отступом_
+ Фон меняется двумя способами:
     1. На [Главной странице](https://scofield001.github.io/diamond/) при **наведении** на элемент:
        1. Создаем элемент, отвечающий за фон рядом с другим элементом,
            растягиваем его на весь экран с помощью _`transform`, `margin` и `padding`_;
        2. Проставляем у убоих элементов _`z-index`_;
        3. Применяем псевдокласс _`hover`_ к родственному(`+`) элементу,
            т.к. изменить элемент обращаясь от дочернего элемента к родителю мы не можем;
     1. В [Альтернативной странице](https://scofield001.github.io/diamond/focus), если элемент получил **фокус**:
        1. Создаем тег **input** и запрещаем ввод c помощью атрибута `readonly`;
        2. Применяем псевдокласс `focus-within` к **контейнеру**;
#### Сжаты
+ ***Изображения*** с помощью `tinify` без потери качества
+ ***html*** с помощью `pug`
+ ***css*** c помощью `sass`, также автоматически добавлены _префиксы_


    sass/
        animations/ # Обработчики анимаций
        blocks/     # БЭМ
        expansions/ # Наследования SASS
        mixins/     # Миксины
        main.scss   # Основные стили
Код *Production* версии находится _[здесь](https://github.com/Scofield001/scofield001.github.io/tree/master/diamond)_
##### Скоро будут добавлены адаптивные изображения

