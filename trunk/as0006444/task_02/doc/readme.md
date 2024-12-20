# Лабораторная работа №2
<p align="center">Министерство образования Республики Беларусь</p>
<p align="center">Учреждение образования</p>
<p align="center">«Брестский государственный технический университет»</p>
<p align="center">Кафедра ИИТ</p>
<br><br><br><br>
<p align="center">Лабораторная работа №2</p>
<p align="center">По дисциплине: «ТИМАУ»</p>
<p align="center">Тема: «Изучение ПИД-регуляторов»</p>
<br><br><br>
<p align="right">Выполнил</p> 
<p align="right">Студент 3-го курса</p>
<p align="right">Группы АС-64</p>
<p align="right">Котковец К.В.</p>
<p align="right">Проверил</p>
<p align="right">Иванюк Д.С.</p>
<br><br><br>
<p align="center">Брест 2024</p>

---

# Лабораторная работа №2. ПИД-регуляторы

**Цель работы:** Изучение принципов работы ПИД-регуляторов и их применения на линейных и нелинейных моделях.

## Описание работы

В данной работе реализованы два типа ПИД-регуляторов:

1. **Линейный ПИД-регулятор (Line_PID)** - использует простую линейную модель для расчета следующего значения отклика.
2. **Нелинейный ПИД-регулятор (Non_line_PID)** - более сложная модель, включающая квадратичную и синусоидальную зависимости.

Каждый из регуляторов вычисляет отклик на основе текущей температуры и подаваемого тепла.

## Основные компоненты

### Классы

- **AbsModPID**: Абстрактный базовый класс для ПИД-регуляторов. Содержит виртуальный метод `calc_PID` для вычисления отклика.
- **Line_PID**: Линейная модель ПИД-регулятора. Наследуется от `AbsModPID`.
- **Non_line_PID**: Нелинейная модель ПИД-регулятора. Наследуется от `AbsModPID`.
- **regulator_detka**: Основной класс, содержащий параметры ПИД-регулятора и реализующий метод для выполнения вычислений и записи результатов в файл.

### Методы

- `calc_PID`: Метод расчета ПИД-регулятора, возвращающий следующее значение температуры.
- `calculation_c_uk`: Метод расчета параметра `c_uk`, используется для получения корректирующего сигнала.

### Использование программы

1. Программа создает файл `results.txt`.
2. Линейная и нелинейная модели рассчитываются на 50 итераций, после чего результаты записываются в файл.
3. Программа выводит сообщение о сохранении данных.

## Результаты работы

Результаты работы программы можно найти в файле `results.txt`. Данный файл содержит значения ошибок `E`, результирующих откликов `Y` и управляющих сигналов `U` для каждой из моделей на каждой итерации.

## Заключение

В ходе работы были исследованы различия в работе линейных и нелинейных ПИД-регуляторов. Полученные результаты демонстрируют разницу в поведении моделей при одинаковых входных условиях.