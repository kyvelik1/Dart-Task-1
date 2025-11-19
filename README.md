# Практическая работа № 3
## Управление потоком выполения кода в языке программирования Dart
>Задание №10 - Описание
```dart
import 'dart:math';
void main() {
  int secret = Random().nextInt(10) +1;
  int guess = 7;
  print("Загадочное число = $secret");
  
  print("Попытка = $guess");
  print("Результат = ${guess == secret}");
}
```
>Задание №11 - Описание
```dart
import 'dart:math';
void main() {
  int secret = Random().nextInt(10) +1;
  int guess = 7;
  print("Загадочное число = $secret");
  
  print("Попытка = $guess");
  print("Результат = ${guess == secret}");
}
```
>Задание №10 - Создайте прогрумму для вычисление стоимости билета в кино: дети до 12 лет - 200 руб, студенты (с удостверением) - 300 руб, взрослые - 500 руб, пенсионеры - 250 руб.
```dart
void main() {
  int child = 200;
  int student= 300;
  int adoult = 500;
  int pensioner = 250;
  
  print("Билет для ребенка = $child руб");
  print("Билет для ребенка = $student руб");
  print("Билет для ребенка = $adoult руб");
  print("Билет для ребенка = $pensioner руб");
}
```
>Задание №11 - Создайте оператор if-cas, напишите программу которая проверяет является ли список двухэлементным списком целых чисел и выводит их сумму.
```dart
void main() {
 var list = [4,7];
  
  if (list case [int a, int b]) {
    
    print("Сумма = ${a+b}");
  } else {
    print("Список не подходит");
  
  }
}
}
```
>Задание №12 - Создайте программу с if-case кооторая проверяет json - объектт на наличие полей "name" (строка) и "age" (Число), и выводит информациюо пользователе.
```dart
void main() {
var user = {
  "name": "Alex", 
  "age": 20
  };
  if (user case {"name": String name, "age": int age}) {
    print("Имя: $name");
    print("Возврат: $age");
  } else {
    print("json объект не содержит нужных полей");
  }
  }
}
```
