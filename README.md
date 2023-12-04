# Алгоритмы кластерного анализа
## Провести необходимые вычисления. Полученные результаты снабдить подробным комментарием. 

## Цель работы: 
выполнить кластерный анализ данных. Провести сравнение различных алгоритмов кластеризации.  Объяснить результаты. 
## Данные: 
в каждом варианте два набора данных X_4_i и  Y_4_i (i – номер варианта). Данные представляют собой векторы-строки в пространстве R4. 
Выполнить первичную обработку данных. Сделать первые выводы.

## Подготовка данных:
для каждого набора данных X_4_i и  Y_4_i  выбрать расстояние в R4 (интересно не только евклидово расстояние).
- вычислить матрицу расстояний 
- перейти к матрице близостей (similarity matrix) и построить графовую модель данных (полный, неориентированный, простой взвешенный граф)

## 1. Кластеризация для числа кластеров k=2.
1.1 Найти разбиение каждого набора данных на 2 кластера с помощью следующих алгоритмов
- Один (на выбор) из алгоритмов иерархической кластеризации: Threshold method=MST method=Single Linkage, Complete Linkage, Average Linkage, Centroid Linkage, Ward Linkage). Можно использовать матрицу близостей или матрицу расстояний. 
- k-means
- EM алгоритм
- Spectral algorithm (использовать матрицу близостей)
1.2 Сравнить попарно разбиения, полученные разными методами с помощью RAND индекса (вычислить RAND индекс для каждой пары разбиений). Дать комментарий к результату. 
1.3 Вычислить значение функции модулярности для каждого разбиения на 2 кластера из п.1.1.
1.4 Сделать общие выводы по возможности разбиения на 2 кластера каждого набора данных.

## 2. Кластеризация для числа кластеров k=3.
2.1 Найти разбиение каждого набора данных на 3 кластера с помощью следующих алгоритмов
- Один (на выбор) из алгоритмов иерархической кластеризации: Threshold method=MST method=Single Linkage, Complete Linkage, Average Linkage, Centroid Linkage, Ward Linkage). Можно использовать матрицу близостей или матрицу расстояний. 
- k-means
- EM алгоритм
- Spectral algorithm (использовать матрицу близостей)
2.2 Сравнить попарно разбиения, полученные разными методами с помощью RAND индекса (вычислить RAND индекс для каждой пары разбиений). Дать комментарий к результату. 
2.3 Вычислить значение функции модулярности для каждого разбиения на 3 кластера из п.2.1.
2.4 Сделать общие выводы по возможности разбиения на 3 кластера каждого набора данных.

## 3. Общий случай.
- предложите (или найдите готовый) способ определения возможного числа кластеров в данных. Примените этот способ к каждому из заданных наборов данный. Сравните с вашими результатами п.1.4 и п.2.4
- Предложите (или найдите в литературе) какой-либо другой критерий качества кластеризации (отличный от модулярности). Сравните разбиения п.1.1 и п.2.1 по этому критерию. Дайте комментарий, как это согласуется с вашими выводами п.1.4 и п.2.4. 


## RAND index
Given a set N of n elements  and two partitions of  N  to compare,  C1 , a partition of N into r subsets, and C2, a partition of N into s subsets, define the following:
•	a , the number of pairs of elements in N that are in the same subset in C1 and in the same subset in C2
•	b, the number of pairs of elements in N that are in different subsets in C1 and in different subsets in C2
•	c, the number of pairs of elements in N that are in the same subset in C1 and in different subsets in C2
•	d, the number of pairs of elements in N that are in different subsets in C1 and in the same subset in C2
The RAND index is       R =(a+b)/(a+b+c+d)
R=1 means that two partition coincide. 
R is close to zero means that two partitions essentially differ.  
