# KSUCTA-SHOP
**Ksucta shop** - разработка интернет-магазина для конкурсной работы по предмету 'Web-программирование'

Разработчики сайта: Кирилл Котюнин ПИН-1-18 и Александр Астанин ПИН-2-18 </br>
Преподаватель: Шеримбекова Эльзат Бактыбековна

#### Структура проекта
Здесь будет описание содержимого сайта - страницы, категории, подкатегории и т.д. </br> 
Этот раздел будет добавляться по мере разработки  html макета.

#### Дизайн проекта
Точный дизайн макет не утверждён, есть наброски:

https://ninjamock.com/s/776R9Tx </br>
https://www.figma.com/file/J0r0cD5u0qbpypyYnsb7PR/maket?node-id=0%3A1 </br>
https://drive.google.com/file/d/1U6PBlAPdsoG56SvaD7T-1yfGWGq-JKLi/view?usp=sharing

Дизайн сайта будет дорабатываться в ходе работы над html шаблоном и его функционалом


## Список применяемых технологий

- GULP. &nbsp;[Документация по настройке GULP](https://gulpjs.com/docs/en/getting-started/quick-start)
- HTML (PUG). &nbsp;[Документация по работе с PUG](https://pugjs.org/api/getting-started.html)
- CSS (SASS). &nbsp;[Документация по работе с SASS](https://sass-lang.com/documentation)
- JS (jQuery)
- Libs (jQuery.js, Slick-slider.js, Normalize.css, FancyBox.js)
- PHP (WordPress + WooCommerce)

## Файловая структура
<ul>
  <li><strong>"Build" папка</strong>: содержит в себе готовый проект</li>
	<li><strong>"Gulp" папка</strong>: содержит в таски для работы gulp-плагинов
    <ul>
			<li><strong>"Config" папка</strong>: экспортирует из всех файлов в соседней папке tasks написанные скрипты</li>
			<li><strong>"Tasks" папка</strong>: хранит в себе файлы тасков для галпа, один таск == один файл</li>
		</ul>
  </li>
	<li><strong>"Src" папка</strong>: содержит в себе файлы для разработки проекта:
		<ul>
			<li><strong>"Pug" папка</strong>: содержит в себе файлы с расширением .pug, которые gulp компилирует в HTML</li>
			<li><strong>"Static" папка</strong>: содержит остальные файлы для разработки (js,scss, fonts, images) </li>
		</ul>
	</li>
</ul>

## GULP - подробно о настройке сборщика проекта и его модулях

Список подключенных модулей для разработки (devDependencies list):
  - "browser-sync": "^2.26.7",
  - "gulp": "^4.0.2",
  - "gulp-autoprefixer": "^7.0.1",
  - "gulp-concat": "^2.6.1",
  - "gulp-csso": "^4.0.1",
  - "gulp-load-plugins": "^2.0.3",
  - "gulp-notify": "^3.2.0",
  - "gulp-pug": "^4.0.1",
  - "gulp-sass": "^4.1.0",
  - "gulp-sourcemaps": "^2.6.5",
  - "gulp-tinypng": "^1.0.2"

#### gulp-pug. [ссылка на источник](https://www.npmjs.com/package/gulp-pug)
Служит для компиляции кода написанного с помощью PUG в обычную HTML разметку

#### gulp-sass. [ссылка на источник](https://www.npmjs.com/package/gulp-sass)
Служит для компиляции кода написанного с помощью SASS в обычный CSS код

#### gulp-csso. [ссылка на источник](https://www.npmjs.com/package/gulp-csso)
Подключается во время компиляции SASS в CSS, удаляет повторяющийся код и минифицирует его

#### gulp-autoprefixer. [ссылка на источник](https://www.npmjs.com/package/gulp-autoprefixer)
Добавляет вендорные префиксы для корректной поддержки css кода разными браузерами

#### gulp-tinypng. [ссылка на источник](https://www.npmjs.com/package/gulp-tinypng)
Оптимизирует изображения в папке src/images

#### gulp-concat. [ссылка на источник](https://www.npmjs.com/package/gulp-concat)
Обьединяет несколько файлов в один

#### gulp-sourcemaps. [ссылка на источник](https://www.npmjs.com/package/gulp-sourcemaps)
Создаёт source-maps в конце css кода

#### gulp-load-plugins. [ссылка на источник](https://www.npmjs.com/package/gulp-load-plugins)
Нужен для автоматизации подключения gulp модулей

#### gulp-notify. [ссылка на источник](https://www.npmjs.com/package/gulp-notify)
Нужен для оповещений об ошибке в коде

#### browser-sync. [ссылка на источник](https://www.browsersync.io/docs/gulp)
Обновляет страницу при наличии изменений в коде

## Инструкция по запуску проекта локально

Клонируем репозиторий к себе на компьютер  </br>
Проверяем наличие nodejs в консоли с помощью команды:

```bash
$ npm -v
```
Если такой команды не найдено, то скачиваем и устанавливаем [nodejs](https://nodejs.org/en/) </br></br>
Проверяем наличие git в консоли с помощью команды:
```bash
$ git --version
```
Если такой команды не найдено, то скачиваем и устанавливаем [git](https://git-scm.com/) </br></br>

1. Открываем папку проекта в командной строке Git Bash </br>
2. Вводим команду: </br>
```bash
$ npm i
```
3. После окончания загрузки, мы можем запустить проект на локальном хосте: [localhost:3000](http://localhost:3000/) с помощью команды:
```bash
$ gulp
```
