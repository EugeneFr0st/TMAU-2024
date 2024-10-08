﻿<p align="center">Министерство образования Республики Беларусь</p>
<p align="center">Учреждение образования</p>
<p align="center">«Брестский Государственный технический университет»</p>       
<p align="center">Кафедра ИИТ</p>
<br><br><br><br>
<p align="center">Лабораторная работа №1</p>
<p align="center">Тема: моделирование управляемого объекта</p>
<br><br><br>
<p align="right">Выполнил:</p>
<p align="right">Студент 3-го курса</p>
<p align="right">Группы АС-63</p>
<p align="right">Мороз Е. В.</p>
<p align="right">Проверила:</p>
<p align="right">Ситковец Я. С.</p>
<br><br><br>
<p align="center">Брест 2024</p>

---


**Цель:** моделирование температуры управляемого объекта с использованием C++. Температура объекта описывается дифференциальным уравнением, и мы реализуем как линейную, так и нелинейную дискретные модели, полученные из этого уравнения.

Исходная функция:
![alt text](Task.png)


Программа выводит смоделированную температуру на каждом временном шаге для обеих моделей - линейной(1) и нелинейной(2). 

![alt text](linear&nonlinear.png)

Код программы находится в папке *src* под названием *main.cpp*

Пример вывода (будет варьироваться в зависимости от параметров):
```markdown
Введите коэффициенты модели (a, b, c, d):
1 2 1 2
Введите начальную температуру: 15
Введите тепловой поток: 10
Введите количество шагов: 5
Выберите модель (1 - линейная, 2 - нелинейная): 1

Результаты моделирования:
-------------------------
Шаг 0: Температура = 15.00°C
Шаг 1: Температура = 35.00°C
Шаг 2: Температура = 55.00°C
Шаг 3: Температура = 75.00°C
Шаг 4: Температура = 95.00°C
Шаг 5: Температура = 115.00°C


Введите коэффициенты модели (a, b, c, d):
1 2 1 2
Введите начальную температуру: 10
Введите тепловой поток: 2
Введите количество шагов: 5
Выберите модель (1 - линейная, 2 - нелинейная): 2

Результаты моделирования:
-------------------------
Шаг 0: Температура = 10.00°C
Шаг 1: Температура = -186.18°C
Шаг 2: Температура = -69509.39°C
Шаг 3: Температура = -9663181229.31°C
Шаг 4: Температура = -186754142950827622400.00°C
Шаг 5: Температура = -inf°C
```

**Вывод:** В ходе выполнения лабораторной работы были протестированы две модели: линейная и нелинейная. Линейная модель показала адекватные результаты с возрастающей температурой на каждом шаге. Однако, при использовании нелинейной модели результаты оказались нестабильными, что привело к некорректным значениям температуры, включая отрицательные и бесконечные значения. Это указывает на необходимость корректировки коэффициентов модели или метода решения для получения более устойчивых результатов.