SET - 3
============

### Задача 1 ###

Напишете програма, която, по дадени координати на 3 точки в двумерна декартова координатна система, намира лицето
на триъгълника, който образуват.

#### Примери ####

```c++
0 0
0 3
4 0
// -> 6

0 0
0.25 0.25
0 0.25
// -> 0.03125
```

### Задача 2 ###

Демонстрирайте с по един пример манипулаторите за извеждане на числа ```showpoint```, ```showpos```, ```setprecision()```,
```fixed```, ```scientific```.

#### Примери ####

Резултатите от примерите предполагат, че всеки ред се изпълнява отделно, тоест коментирайте с ```//``` всички редове освен
този, който искате да се изпълни.

```c++
cout << 10.0;               // -> 10
cout << showpoint << 10;    // -> 10
cout << showpoint << 10.0;  // -> 10.0

cout << 9;              // -> 9
cout << showpos << 9;   // -> +9
cout << -9;             // -> -9
cout << showpos << -9;  // -> -9

cout << 9.87654321;                // -> 9.87654
cout << fixed << 9.87654321;       // -> 9.876543
cout << scientific << 98.7654321;  // -> 9.876543e+001

cout << setprecision(3) << 9.87654321;                // -> 9.88
cout << setprecision(3) << fixed << 9.87654321;       // -> 9.877
cout << setprecision(3) << scientific << 98.7654321;  // -> 9.877e+001
```

### Задача 3 ###

Напишете програма, която намира и извежда на екрана цифрите на, въведено от клавиатурата, 3-цифрено цяло число.

#### Примери ####

```c++
340
// -> Hundreds: 3
//    Tens: 4
//    Units: 0

424
// -> Hundreds: 4
// -> Tens: 2
// -> Units: 4

579
// -> Hundreds: 5
// -> Tens: 7
// -> Units: 9
```

### Задача 4 ###

Напишете програма, която разменя стойностите на две целочислени променливи без използването на помощна променлива.

#### Забележка ####

Защо не е хубаво да правите размяна на стойности по този начин?

Най-често областта от стойности на типа ```int``` е ```[-2^31, 2^31 - 1]```  (зависи от компилатора). Тоест, ако имаме променлива
от тип ```int``` със стойност ```2^31 - 1``` и към нея прибавим ```1```, ще излезем извън областта и стойността на променливата
ще стане ```-2^31```, тоест ще се върнем в началото на областта. Аналогично, ако стойността е  ```-2^31``` и извадим от нея ```1```
ще отидем в края на областта - ```2^31 - 1```.

### Задача 5 ###

Докажете чрез пример истинността на обясненото в [забележката на задача 4](https://github.com/gshopov/up2013/tree/master/exercises/exercise1#%D0%97%D0%B0%D0%B1%D0%B5%D0%BB%D0%B5%D0%B6%D0%BA%D0%B0).

#### Забележка ####

Функцията ```pow``` връща резултат от тип ```double```. Когато присвояваме този ```double``` резултат на променлива от тип ```int```
резултатът се закръгля **надолу**, за да получим цяло число. Препоръчва се това да става явно, тоест ние да покажем чрез кода, че това
наистина ще се случи. Затова поставяме ```(int)``` пред израза.

### Задача 6 ###

Използвайки метаезика на Бекус-Наур, дайте дефиниции на **реално число** и **име на променлива**.
