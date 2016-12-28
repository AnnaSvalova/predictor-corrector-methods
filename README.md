Домашняя работа №3
==================

В рамках домашней работы №3 я выбрала реализацию предикторно-корректорных 
методов.

Последовательная реализация
---------------------------
В файле **sequential.c** исходники для последовательной реализации.

*Результат вычислений:*

    x[0] = 1.372303
    x[1] = 0.793119
    x[2] = 1.370595
    x[3] = 0.784629
    x[4] = 1.359385
    x[5] = 0.782821
    x[6] = 1.354142
    x[7] = 0.790142
    x[8] = 1.362077
    x[9] = 0.796556

*Время вычисления:*

    1m11.525s

Параллельная реализация
-----------------------
В файле **parallel.c** - параллельная реализация с использованием openmp.

*Результат вычислений:*

    x[0] = 1.363691
    x[1] = 0.789456
    x[2] = 1.363691
    x[3] = 0.789456
    x[4] = 1.363691
    x[5] = 0.789455
    x[6] = 1.363691
    x[7] = 0.789455
    x[8] = 1.363691
    x[9] = 0.789455

*Время вычислений:*

    0m58.199s

Вопросы:
--------

* Какой порядок сходимости методов?

У последовательного алгоритма второй порядок точности.
У параллельного алгоритма. Так как этот метод базируется на методах второго
порядка, то он сам имеет порядок не выше второго.

* Не привело ли внесение внутреннего параллелизма к снижению точности по 
  сравнению с последовательным методом?

Мне кажется, точность снизилась.

* Ускорение?

Согласно результатам, скорость вычисления сократилась примерно на 15-20%.