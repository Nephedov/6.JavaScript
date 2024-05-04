# Домашнее задание к лекции 6 «Обработка исключений и замыкания»

## Решения
 * <a href="https://github.com/Nephedov/bjs-2-homeworks/blob/bjs-53/6.exception-closure/task.js">task.js</a> - код с реализованными функциями.

<a href="https://github.com/Nephedov/bjs-2-homeworks/tree/bjs-53/6.exception-closure">Репозиторий</a> с заданием и тестами.
Запуск через <a href="https://github.com/Nephedov/bjs-2-homeworks/blob/bjs-53/6.exception-closure/index.html">index.html</a>.

## Что было сделано
* Написаны функции распарсивающие строку в число с плавающей точкой, либо генерирующие ошибку в противном случае.
* Написан класс Triangle, экземпляр которого имеет методы расчета периметра и площади треугольника, в случае правильного треугольника. В противном случае генерирует ошибку.
* Решение задания опубликовано в Github Pages.

## Задача 1. Форматтер чисел
Ошибки случаются, и нужно уметь с ними работать. Ваши коллеги разработали форму, которая принимает от пользователя количество покупаемых единиц товара. Вас попросили написать функцию-преобразователь, которая:

* возвращает число, если всё корректно;
* генерирует ошибку, если ввод не является числом в десятичной системе счисления.

## Задача 2. Треугольник 
На этот раз Вася решил создать онлайн-калькулятор геометрических фигур. Помогите ему создать калькулятор треугольников, который сможет проверять существование треугольника, считать площадь и периметр.

### Что нужно сделать
1. Напишите класс `Triangle`.
    * Конструктор класса должен принимать три стороны треугольника.
    * В случае нарушения правила существования треугольника (сумма двух сторон меньше третьей) выбрасывайте исключение с ошибкой *«Треугольник с такими сторонами не существует»*.
    * Геттер `perimeter` должен возвращать периметр треугольника.
    * Геттер `area` должен возвращать площадь треугольника. Для подсчёта площади используйте [формулу Герона](https://ru.wikipedia.org/wiki/%D0%A4%D0%BE%D1%80%D0%BC%D1%83%D0%BB%D0%B0_%D0%93%D0%B5%D1%80%D0%BE%D0%BD%D0%B0). Точность должна вычисляться с обозначением до трёх знаков после запятой.
2. Напишите функцию `getTriangle`.
    * Аргументами функции являются три значения длин сторон.
    * Попытайтесь вернуть новый объект треугольника.
    * В случае перехвата исключения возвращайте объект с двумя геттерами `area` и `perimeter`, которые возвращают строку: *«Ошибка! Треугольник не существует»*.
