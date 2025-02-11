# Распознавание изображения web камеры в реальном времени

Испольюзуется библиотека компьютерного зрения [OpenCV](https://github.com/opencv/opencv/tree/master) и [признаки Харра](https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B8%D0%B7%D0%BD%D0%B0%D0%BA%D0%B8_%D0%A5%D0%B0%D0%B0%D1%80%D0%B0)

## Как установить

Для запуска скриптов у вас уже должен быть установлен Python 3.

- Скачайте код
- Установите библиотеки командой `pip install -r requirements.txt`

## Как запустить

`python3 run.py`

## Папка haarcascades

Содержит обученные классификаторы для обнаружения объектов определенного типа, т.е. лица (анфас, профиль), кошки и т.д.

## config.py

Словарь с настройками для распозноваемых объектов:

* `path` - путь к XML файлу Харра;
* `color` - цвет прямоугольной рамки в цветовом пространстве RGB;
* `draw` - отображать рамку (`True`) или нет (`False`).

![config](https://user-images.githubusercontent.com/58470881/192338234-3174c55a-26b3-492f-b726-e1e669022d7c.png)

## run.py

Если web камера не найдена, то ошибка:

![web not find](https://user-images.githubusercontent.com/58470881/192338295-eb3d97e2-9863-414b-8ee0-c0d5cfdadc65.png)

Пример распознования глаз, после нажатия правой кнопки мыши появляется меню:

![menu](https://user-images.githubusercontent.com/58470881/192338359-ebacbd56-8711-4c8d-8ac2-8846edb34bd9.png)

В нижнем левом углу отображаются координаты курсора и цвет пикселя в пространстве RGB.

`q` - завершение скрипта
