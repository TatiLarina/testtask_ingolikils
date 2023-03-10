# План тестирования
## Возможные варианты результата:

1) равносторонний треугольник (А=Б=С)

2) равнобедренный треугольник (А=Б или А=С или Б=С)

3) разносторонний треугольник (стороны не равны)

4) треугольника не существует ((А+Б) <= C или (А+С)<=Б или (Б+С) <= А)

## Следовательно необходимо протестировать: ##

1. Валидные варианты значений 1, 2, 3

* Целые числа
* Дробные числа

2. Варианты с несуществующим треугольником 4
3. Проверить поля на невалидные значения: 

*  Отрицательные числа
* Ноль
* Любые символы кроме цифр и "." (латиница, кириллица, пробел, другие символы)
* Вариант с цифрами и двумя точками
* Ввод предельного количества цифр (уточнить по спецификации или ТЗ)
  
4. Проверить невозможность ввода чего-либо в поле "Результат"

# Примеры тест-кейсов

Тест-кейс 1. Равностороний треугольник
1. Шаги: Ввести в поля А, Б и С значение 30
2. Ожидаемый результат: в поле "Результат" "Равносторонний треугольник"

Тест-кейс 2. Разностороний треугольник
1. Шаги: Ввести в поле А 10, в поле Б 12, в поле С 14.
2. Ожидаемый результат: в поле "Результат" "Равносторонний треугольник"

Тест-кейс 3. Треугольник не существует
1. Шаги: Ввести в поле А 10, в поле Б 20, в поле С 30.
2. Ожидаемый результат: в поле "Результат" "Треугольника не существует"

Тест-кейс 4. Отрицательное число в поле А
1. Шаги: Ввести в поле А -10, в поле Б 20, в поле С 20
2. Ожидаемый результат: сообщение об ошибке и просьба ввести положительное число