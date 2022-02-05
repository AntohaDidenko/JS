# JS

Всем здрасти :ура:
Массивы являются одной из самых часто встречающихся структур данных в JS, они используются для хранения данных. Также массивы дают много возможностей для работы с данными.
Функции позволяют повторять одно и то же действие во многих частях программы. Это как основной строительный элемент.
Если кратко подытожить - массивы и функции являются одной из самых основных тем и с ними часто придется встречаться в работе.
=========Очень важно не забывать о том, что наши методы работы с массивами как и условия, могут что-то возвращать.
=========Индексация в массиве начинается с 0.
=========С помощью свойства length мы можем получить длину массива или строки (возвращает число), будет полезно при вычислении последнего индекса массива.
=========Шпаргалка по методам массивов:

<!-- split/join – преобразует строку в массив и обратно.
push () – добавляет элементы в конец,
pop() – удаляет элемент с конца,
shift() – удаляет элемент с начала,
unshift() – добавляет элементы в начало.
splice(index, deleteIndex, ...arr) – начиная с индекса index, удаляет deleteIndex элементов и вставляет arr.
slice(start, end) – создаёт новый массив, копируя в него элементы с позиции start до end (не включая end). -->

=========Функция должна делать только то, что явно подразумевается её названием. И это должно быть одним действием. Если кратко и понятно: Одна функция – одно действие.
=========Шпаргалка по объявления функций в JS:
Функциональное выражение (function expression)
const greet = function (name) {
return `Hello, ${name}`;
};
Объявление функции (function declaration)
function greet(name) {
return `Hello, ${name}!`;
}
=========Для того чтобы что-то вернуть из функции/метода или из условия, можно использовать оператор return. Так же из функции можно возвращать сразу любой типа данных, например
return 'hello' // (вернем строку)
или
return true // (вернем буль)
или
return [1, 2] // (вернем массив)
=========Паттерн ранний возврат, говорит о том, что если условие внутри нашего if вернет true, то нам сразу же нужно что-то вернуть из тела этого условия, с помощью return.
=========Не забывайте что оператор = это оператор присвоения, а не сравнения
=========Несколько лайфхаков при работе с массивами
Как быстро очистить массив
const fruits = ['banana', 'apple', 'orange', 'watermelon', 'apple', 'orange', 'grape', 'apple'];
fruits.length = 0;
console.log(fruits); // вернет []

Как объединить более двух массивов
const fruits = ['apple', 'banana', 'orange'];
const meat = ['poultry', 'beef', 'fish'];
const vegetables = ['potato', 'tomato', 'cucumber'];
const food = [...fruits, ...meat, ...vegetables];
console.log(food); // вернет ["apple", "banana", "orange", "poultry", "beef", "fish", "potato", "tomato", "cucumber"]

Как получить рандомное значение массива
const fruits = [
'banana',
'apple',
'orange',
'watermelon',
'apple',
'orange',
'grape',
'apple',
];
const randomFruit = fruits[Math.floor(Math.random() * fruits.length)];
console.log(randomFruit); // вернет рандомный фрукт из массива
