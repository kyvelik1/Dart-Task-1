import 'dart:math';

void main() {
  print('=== Блок 1: Целое число (int) ===');
  task1(); task2(); task3(); task4(); task5();
  task6(); task7(); task8(); task9(); task10();

  print('\n=== Блок 2: Дабл (double) ===');
  task11(); task12(); task13(); task14(); task15();
  task16(); task17(); task18(); task19(); task20();

  print('\n=== Блок 3: Строки (String) ===');
  task21(); task22(); task23(); task24(); task25();
  task26(); task27(); task28(); task29(); task30();

  print('\n=== Блок 4: Логическое значение (bool) ===');
  task31(); task32(); task33(); task34(); task35();

  print('\n=== Блок 5: Списки (List) ===');
  task36(); task37(); task38(); task39(); task40();

  print('\n=== Блок 6: Словари (Map) ===');
  task41(); task42(); task43(); task44(); task45();

  print('\n=== Блок 7: Множества (Set) ===');
  task46(); task47(); task48(); task49(); task50();
}

// --- Блок 1 ---
void task1() {
  int a = 15, b = 4;
  print('1. Сумма: ${a + b}, Разность: ${a - b}, Произведение: ${a * b}, Деление: ${a ~/ b}, Остаток: ${a % b}');
}
void task2() {
  int number = 7;
  print('2. $number - ${number % 2 == 0 ? 'чётное' : 'нечётное'} число');
}
void task3() {
  int number = 5;
  print('3. Куб числа $number = ${number * number * number}');
}
void task4() {
  int number = -42;
  print('4. Абсолютное значение $number = ${number.abs()}');
}
void task5() {
  int n = 5, factorial = 1;
  for (int i = 1; i <= n; i++) factorial *= i;
  print('5. Факториал $n = $factorial');
}
void task6() {
  int number = 50;
  print('6. $number ${number >= 10 && number <= 100 ? 'находится' : 'не находится'} в диапазоне [10, 100]');
}
void task7() {
  int number = 456;
  int sum = number.toString().split('').map(int.parse).reduce((a, b) => a + b);
  print('7. Сумма цифр $number = $sum');
}
void task8() {
  int number = 12345;
  print('8. Количество цифр: ${number.toString().length}');
}
void task9() {
  int number = 12321;
  String strNum = number.toString();
  print('9. $number - ${strNum == strNum.split('').reversed.join('') ? 'палиндром' : 'не палиндром'}');
}
void task10() {
  int a = 10, b = 25, c = 15;
  print('10. Максимум: ${max(a, max(b, c))}, Минимум: ${min(a, min(b, c))}');
}

// --- Блок 2 ---
void task11() {
  double x = 7.5, y = 2.5;
  print('11. Сумма: ${x+y}, Разность: ${x-y}, Произведение: ${x*y}, Деление: ${x/y}');
}
void task12() {
  double radius = 5.0;
  print('12. Площадь круга = ${pi * radius * radius}');
}
void task13() {
  double radius = 3.0;
  print('13. Периметр = ${(2 * pi * radius).toStringAsFixed(2)}');
}
void task14() {
  double celsius = 25.0;
  print('14. $celsius°C = ${celsius * 1.8 + 32}°F');
}
void task15() {
  double number = 3.7;
  print('15. ceil=${number.ceil()}, floor=${number.floor()}, round=${number.round()}, toInt=${number.toInt()}');
}
void task16() {
  double a = 10.5, b = 20.3, c = 15.2;
  print('16. Среднее: ${((a + b + c) / 3).toStringAsFixed(2)}');
}
void task17() {
  double a = 5.0, b = 6.0, c = 7.0;
  double p = (a + b + c) / 2;
  print('17. Площадь треугольника = ${sqrt(p * (p - a) * (p - b) * (p - c)).toStringAsFixed(2)}');
}
void task18() {
  double x1 = 0, y1 = 0, x2 = 3, y2 = 4;
  print('18. Расстояние = ${sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2))}');
}
void task19() {
  double normal = 10.5;
  print('19. isFinite: ${normal.isFinite}, isInfinite: ${double.infinity.isInfinite}, isNaN: ${double.nan.isNaN}');
}
void task20() {
  double amount = 1000.0, percent = 15.0;
  print('20. $percent% от $amount = ${amount * (percent / 100)}');
}

// --- Блок 3 ---
void task21() {
  String text = 'Flutter';
  print('21. Длина: ${text.length}, Первый: ${text[0]}, Последний: ${text[text.length - 1]}');
}
void task22() {
  String name = 'Иван', city = 'Москва'; int age = 25;
  print('22. Мое имя $name, мне $age лет, я из города $city');
}
void task23() {
  String text = 'DaRt PrOgRaMmInG';
  print('23. ${text.toUpperCase()} / ${text.toLowerCase()}');
}
void task24() {
  String text = 'Hello, Dart!';
  print('24. "Dart" найдено в позиции ${text.indexOf('Dart')}');
}
void task25() {
  String text = 'Programming Language';
  print('25. Первые 5: ${text.substring(0, 5)}, Последние 4: ${text.substring(text.length - 4)}');
}
void task26() {
  String csv = 'apple,banana,cherry,date';
  print('26. Разбиение: ${csv.split(',')}');
}
void task27() {
  String word1 = 'Hello', word2 = 'World', word3 = 'Dart';
  print('27. $word1 $word2 $word3');
}
void task28() {
  String text = 'racecar';
  print('28. "$text" - ${text.toLowerCase() == text.split('').reversed.join('').toLowerCase() ? 'палиндром' : 'не палиндром'}');
}
void task29() {
  String text = 'Programming'.toLowerCase();
  int v = 0, c = 0;
  for (int i = 0; i < text.length; i++) {
    if ('aeiou'.contains(text[i])) v++;
    else if (RegExp(r'[a-z]').hasMatch(text[i])) c++;
  }
  print('29. Гласных: $v, Согласных: $c');
}
void task30() {
  String text = '  Hello   World  ';
  print('30. Без лишних пробелов: "${text.trim().replaceAll(RegExp(r'\s+'), ' ')}"');
}

// --- Блок 4 ---
void task31() {
  bool a = true, b = false;
  print('31. a && b: ${a && b}, a || b: ${a || b}, !a: ${!a}');
}
void task32() {
  int x = 10, y = 20;
  print('32. x > 5 && y > 15: ${x > 5 && y > 15}, x < 5 || y < 15: ${x < 5 || y < 15}');
}
void task33() {
  String pass = 'MyPass123';
  bool isValid = pass.length >= 8 && pass.contains(RegExp(r'\d')) && pass.contains(RegExp(r'[A-Z]'));
  print('33. Пароль валидный: $isValid');
}
void task34() {
  int age = 18;
  print('34. Статус: ${age >= 18 ? 'взрослый' : 'ребёнок'}');
}
void task35() {
  bool? value;
  print('35. Результат: ${value ?? false}');
}

// --- Блок 5 ---
void task36() {
  List<int> numbers = [10, 20, 30, 40, 50];
  print('36. Элементы: $numbers, Длина: ${numbers.length}');
}
void task37() {
  List<String> fruits = ['apple', 'banana'];
  fruits.addAll(['cherry', 'date']);
  fruits.remove('banana');
  print('37. Список: $fruits');
}
void task38() {
  List<int> numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  print('38. Четные: ${numbers.where((n) => n % 2 == 0).toList()}');
}
void task39() {
  List<int> numbers = [1, 2, 3, 4, 5];
  print('39. Квадраты: ${numbers.map((n) => n * n).toList()}');
}
void task40() {
  List<int> numbers = [3, 1, 4, 1, 5, 9, 2, 6];
  numbers.sort();
  print('40. Отсортирован и развернут: ${numbers.reversed.toList()}');
}

// --- Блок 6 ---
void task41() {
  Map<String, int> grades = {'Иван': 85, 'Мария': 92, 'Петр': 78};
  print('41. Оценки: Иван=${grades['Иван']}, Мария=${grades['Мария']}, Петр=${grades['Петр']}');
}
void task42() {
  Map<String, String> capitals = {'Франция': 'Париж', 'Германия': 'Берлин'};
  capitals['Испания'] = 'Мадрид';
  capitals['Франция'] = 'Версаль';
  print('42. Обновленная карта: $capitals');
}
void task43() {
  Map<String, int> prices = {'apple': 50, 'banana': 30, 'cherry': 80};
  print('43. Итерация:');
  prices.forEach((item, price) => print('    $item: $price руб'));
}
void task44() {
  Map<String, int> scores = {'test1': 65, 'test2': 85, 'test3': 75, 'test4': 55};
  scores.removeWhere((key, value) => value <= 70);
  print('44. Фильтрация (>70): $scores');
}
void task45() {
  Map<String, int> map1 = {'a': 1, 'b': 2}, map2 = {'c': 3, 'd': 4};
  print('45. Слияние: ${{...map1, ...map2}}');
}

// --- Блок 7 ---
void task46() {
  Set<int> numbers = {1, 2, 3, 4, 5, 5, 4, 3};
  print('46. Уникальные элементы: $numbers, Размер: ${numbers.length}');
}
void task47() {
  Set<String> c1 = {'red', 'green', 'blue'}, c2 = {'blue', 'yellow', 'purple'};
  print('47. Объединение: ${c1.union(c2)}');
}
void task48() {
  Set<int> s1 = {1, 2, 3, 4, 5}, s2 = {4, 5, 6, 7, 8};
  print('48. Пересечение: ${s1.intersection(s2)}');
}
void task49() {
  Set<String> f1 = {'apple', 'banana', 'cherry'}, f2 = {'banana', 'date'};
  print('49. Разность (в f1, но не в f2): ${f1.difference(f2)}');
}
void task50() {
  List<Map<String, dynamic>> students = [
    {'name': 'Иван', 'grade': 85},
    {'name': 'Мария', 'grade': 92},
    {'name': 'Петр', 'grade': 78},
    {'name': 'Анна', 'grade': 88}
  ];
  var filtered = students.where((s) => s['grade'] > 80).toList();
  filtered.sort((a, b) => b['grade'].compareTo(a['grade']));
  print('50. Лучшие студенты:');
  for (var s in filtered) {
    print('    ${s['name']}: ${s['grade']}');
  }
}
