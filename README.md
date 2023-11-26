# Hello!
## **В этом файле содержится описание решения контрольной работы.**

### *Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.*

* Для начала создадим массив строк "array". В него поместим некоторые значения: 
    
        string[] array = {"Hello", "2", "world", ":-)"}

 Далее создадим метод "NewArray", который будет принимать на вход наш массив и возвращать новый с размерами элементов меньше, либо равным 3. 

* В самом методе укажем значение "value" равное 3, согласно условию. Также добавим счётчик "count" для подсчёта элементов меньших, либо равным 3. Счётчик нужен для того, чтобы задать размер нового массива.

* Далее подсчитываем количество элементов <= 3. Для этого перебираем массив "array" с помощью цикла for (создаём дефолтный цикл for:

         ( i = 0; i < array.Length; i++).

    Находим эти элементы с помощью условного оператора if, в условие записываем сравнение длинны элемента (в данном случае строки) с "value":

        array[i].Length <= value.

* После подсчёта "count" создадим новый массив "resultArray" с длинной "count". Добавим индекс "j" для перебора нового массива. 

* Далее создадим аналогичный раннему цикл for, но уже для записи значений из первого массива в новый. Добавим условие аналогичное условие if: 

        (array[i].Length <= value). 
    Но при выполнении условия мы будем записывать в новый массив значения из первого массива:
    
         resultArray[j] = array[i]; и увеличим индекс на 1 (j++). 

После выполнения цикла сделаем проверку и посмотрим что получилось при выводе: 

        for (int i = 0; i < resultArray.Length; i++) 
        {
            Console.Write(resultArray[i] + " ");
        }       



![скриншот](image-2.png)

Работает.

Вернём новый массив

    return resultArray;

 В блоке Main вызовем наш метод 
 
     NewArray(array);
 
 Готово.

[Ссылка](https://drive.google.com/file/d/12aYUMiqZGeGK7f7pP06MIJS1VkD6gVS2/view?usp=sharing) на блок-схему гугл диск.