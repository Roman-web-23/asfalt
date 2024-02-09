# Gulp сборка 2023
Gulp 4 сборка. HTML, SCSS, JS, webpack, babel, webp, сжатие графики, автопрефиксы

Демо:
https://serrjik.github.io/Gulp2023/

![Скриншот страницы](https://github.com/Serrjik/Gulp2023/blob/main/page.jpg)

Сборка создана по инструкции школы [Webcademy](https://webcademy.ru/). Урок на Youtube: https://youtu.be/D_HW-tvyKKE

## Для чего использовать сборку?

Использовать сборку предполагается для вёрстки многостраничных сайтов. Используется импорт HTML-файлов и препроцессор SCSS для CSS-стилей.

## Как устроена сборка?
* Исходные файлы проекта лежат в папке src. Конечные файлы при разработке падают в папку `build`. При запуске сборки командой `gulp` папка `build` очищается. Это не полностью сжатая версия сайта для разработки.
* При запуске сборки командой `gulp docs` обработанные файлы помещаются в папку `docs` чтобы можно было настроить отображение результата работы сборки на github pages. Это финальная, полностью сжатая версия сайта.
* Настроено слежение и копирование: изображений (папка `src\img`), скриптов (папка `src\js`).
* В финальной версии автоматически создаются копии изображений в формате `webp`.
* Настроено автоматическое добавление префиксов CSS-свойств и создание карт исходных стилей (в каком SCSS-файле и в какой строке изначально было написано CSS-свойство).

## Как использовать сборку:

1. На компьютере должен быть установлен Node Package Manager.

2. Клонировать на локальный ПК репозиторий командой:

`git clone https://github.com/Serrjik/Gulp2023.git`

3. Из папки Gulp2023 вызвать командную строку (например Git Bash), и ввести команду `npm i` для инициализации проекта. Подождать пока будут установлены необходимые пакеты.

4. Запустить сборку командой `gulp` для разработки
   либо командой `gulp docs` для получения готовой для работы версии.

6. Сборка запустится вместе с демонстрационными данными. Нужно удалить ненужные для вашего проекта файлы и отредактировать содержимое основных файлов (`main.scss`, `index.html`, `index.js`).

### Структура папок

1. В папке `src\html` - html-шаблоны HTML-страниц сайта

    1. В папке `src\html\` - шаблоны страниц сайта
    2. В папке `src\html\blocks` - шаблоны частей страниц сайта. Эти шаблоны не компилируются в отдельные файлы

2. В папке `src\scss` - SCSS стили
   
    1. В папке `src\scss\base` - базовые стили (контейнеры, `reset.css`, липкий подвал, утилитарные классы, CSS-переменные)
    2. В папке `src\scss\blocks` - стили блоков (частей страниц) сайта

4. В папке `src\img` - картинки сайта

5. В папке `src\js` - скрипты сайта
