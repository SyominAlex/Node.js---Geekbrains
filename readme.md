# Node.JS
- Курс Geekbrains по Node.JS
- Старт: 30.11.2021
- Преподаватель: Артём Шашков
- Студент: Алексей Сёмин

## Урок 1. Введение в Node.js. Управление зависимостями
[https://gb.ru/lessons/190653/homework](https://gb.ru/lessons/190653/homework)

**Задача 1.** Напишите программу для вывода в консоль простых чисел, чтобы они попадали в указанный диапазон включительно. При этом числа должны окрашиваться в цвета по принципу светофора:
первое число выводится зелёным цветом;
второе — жёлтым;
третье — красным.
Диапазон, куда попадут числа, указывается при запуске программы.
Если простых чисел в диапазоне нет, нужно, чтобы программа сообщила об этом в терминале красным цветом.
Если аргумент, переданный при запуске, не считается числом — сообщите об этом ошибкой и завершите программу.
- **Запуск решения:**
_**npm run hw1 1 100**_ выполнится скрипт из package.json "hw1": "node ./01/ColoredNumbers.js", передаваемые параметры 1 и 100 (здесь для примера) - любые числа.

## Урок 2. Цикл событий. События в Node.js
[https://gb.ru/lessons/190654/homework
](https://gb.ru/lessons/190654/homework)

**Задача 1.** Решите задачу по выводу данных в консоль.
```
console.log('Record 1');

setTimeout(() => {
  console.log('Record 2');
  Promise.resolve().then(() => {
    setTimeout(() => {
      сonsole.log('Record 3');
      Promise.resolve().then(() => {
        console.log('Record 4');
      });       
    });
  });       
});

console.log('Record 5');

Promise.resolve().then(() => Promise.resolve().then(() => console.log('Record 6')));
```
- **Ответ:** в консоль выведет: 1, 5, 6, 2, 3, 4.
- **Запуск решения:**
  _**npm run hw2_1**_ выполнится скрипт из package.json "hw2_1": "node ./02/sync_async.js".

**Задача 2.** Напишите программу, которая будет принимать на вход несколько аргументов: дату и время в формате «час-день-месяц-год». Задача программы — создавать для каждого аргумента таймер с обратным отсчётом: посекундный вывод в терминал состояния таймеров (сколько осталось). По истечении какого-либо таймера, вместо сообщения о том, сколько осталось, требуется показать сообщение о завершении его работы. Важно, чтобы работа программы основывалась на событиях.
- **Запуск решения:**
  _**npm run hw2_2**_ выполнится скрипт из package.json "hw2_2": "node ./02/timer.js 20-15-12-2021 00-01-01-2022", передаваемые параметры - время и дата в формате "час-день-месяц-год".

## Урок 3. Работа с файловой системой. Класс Buffer. Модуль Streams
[https://gb.ru/lessons/190655/homework
](https://gb.ru/lessons/190655/homework)

**Задача 1.** По [ссылке](https://drive.google.com/file/d/1A8B0eDEagkO6XlpJAinsk8_9qQTsnVly/view) вы найдете файл с логами запросов к серверу весом более 2 Гб. Напишите программу, которая находит в этом файле все записи с ip-адресами 89.123.1.41 и 34.48.240.111, а также сохраняет их в отдельные файлы с названием “%ip-адрес%_requests.log”.
- **Запуск решения:**
  _**npm run hw3**_ выполнится скрипт из package.json "hw3": "node index.js".

## Урок 4. CLI-приложения
[https://gb.ru/lessons/190656/homework](https://gb.ru/lessons/190656/homework)

**Задача 1.** В домашнем задании вам нужно будет применить полученные знания к программе, которую вы написали по итогам прошлого урока.
Для этого превратите её в консольное приложение, по аналогии с разобранным примером и добавьте следующие функции:
* Возможность передавать путь к директории в программу. Это актуально, когда вы не хотите покидать текущую директорию, но вам необходимо просмотреть файл, находящийся в другом месте;
* В содержимом директории переходить во вложенные каталоги;
* При чтении файлов искать в них заданную строку или паттерн.

**Запуск решения:**
    _**npm run hw4**_ выполнится скрипт из package.json "hw4": "node index.js".

## Урок 5. HTTP-cервер на Node.js
[https://gb.ru/lessons/190657/homework](https://gb.ru/lessons/190657/homework)

**Задача 1.** Используйте наработки из домашнего задания прошлого урока для того, чтобы создать веб-версию приложения. При запуске она должна:
* Показывать содержимое текущей директории;
* Давать возможность навигации по каталогам из исходной папки;
* При выборе файла показывать его содержимое.

**Запуск решения:**
_**npm run hw5**_ выполнится скрипт из package.json "hw5": "node ./05/index.js".
