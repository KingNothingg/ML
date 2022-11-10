## Постановка задачи

Я выбрал набор данных [Water quality](https://www.kaggle.com/datasets/mssmartypants/water-quality) для выполнения лабораторной работы. Требуется предсказать, является ли вода безопасной или нет.

## Описание работы

В ЛР 0 проведена обработка и анализ данных:

* анализ на наличие нецельных данных
* проверка типа признаков (все они оказались числовыми, было 2 строковых значения NAN, которые я  удалил)
* анализ попарных зависимостей
* анализ корреляционной матрицы
* анализ распределений данных(данные оказались распределены в основном плохо, что повлияло на конченый результат в лр1)
* аугментация данных(классы были сильно несбалансированы, без аугментации recall в лр1 был 30%, после добавления нормально распределенных данных с заданными матожиданием и дисперсией recall вырос до 80-90%)

В ЛР 1 реализованы четыре алгоритма классического машинного обучения:

* метод k-ближайших соседей
* логистическая регрессия
* метод опорных векторов
* наивный байесовский классификатор

Каждый из них сравнивается с готовым из библиотеки scikit-learn.

## Вывод

Набор данных не очень хорошо разделим линейными моделями. Изначальная accuracy была 90%, однако в такой задаче очень важен recall, так как нельзя классифицировать опасную воду как безопасную. После аугментации стало лучше, но это все равно не привело датасет к отличной разделимости.
