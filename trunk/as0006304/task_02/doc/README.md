<p align="center"> Министерство образования Республики Беларусь</p>
<p align="center">Учреждение образования</p>
<p align="center">“Брестский Государственный технический университет”</p>
<p align="center">Кафедра ИИТ</p>
<br><br><br><br><br><br><br>
<p align="center">Лабораторная работа №2</p>
<p align="center">По дисциплине “Теория и методы автоматического управления”</p>
<p align="center">Тема: “ПИД-регуляторы”</p>
<br><br><br><br><br>
<p align="right">Выполнил:</p>
<p align="right">Студент 3 курса</p>
<p align="right">Группы АС-63</p>
<p align="right">Грицук П.Э.</p>
<p align="right">Проверил:</p>
<p align="right">Иванюк Д. С.</p>
<br><br><br><br><br>
<p align="center">Брест 2024</p>

---

## Цель работы:  
Создать программу на C++, которая будет моделировать работу ПИД-регулятора. В качестве объекта управления использовать математическую модель, полученную в предыдущей работе. Программа должна быть реализована с использованием объектно-ориентированного подхода и содержать не менее трех классов, включая наследование. В отчете необходимо предоставить графики для различных температурных заданий объекта, а также предоставить пояснения к полученным результатам. Отчет должен быть сгенерирован с помощью Doxygen в формате .md.

## Реализация  
В результате работы была разработана программа, моделирующая работу ПИД-регулятора. Документация к проекту была подготовлена с использованием Doxygen и сохранена в файле `doxygen.md`. 

Результаты работы программы следующие:  
- Описание поведения ПИД-регулятора в зависимости от различных параметров.
- Графики для различных температурных заданий объекта.
- Пояснения к полученным результатам, включая анализ точности работы регулятора и его отклонений при изменении параметров.

Дополнительно в отчете приведены выводы о влиянии настроек ПИД-контроллера на стабильность системы управления.

## Результаты  
### Линейная модель:  
При следующих значениях: T = 10, TP = 10, TM = 50, K = 0.1  
Желаемое значение W = 5, A = 0.333, B = 0.667  
![linear](./image/linear.png)

### Нелинейная модель: 
При следующих значениях: T = 10, TP = 10, TM = 50, K = 0.1  
Желаемое значение W = 5, A = 1, B = 0.0033, C = 0.525, D = 0.525
![nonLinear](./image/nonLinear.png)