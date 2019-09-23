# Домашняя работа №0

Домашняя работа сдаётся на собеседовании после второй лекции и влияет на поступление на спецкурс

Дата сдачи: (будет определено позднее)

## Задание

Реализовать на языке С/С++ функцию копирования памяти, 
которая имеет следующий [прототип](https://ru.wikipedia.org/wiki/Прототип_функции):

```C
errno_t my_memcpy_s(void *restrict dest, rsize_t destsz, const void *restrict src, rsize_t count ).
```

  * Сравнить скорость работы my_memcpy_s с функцией memcpy_s из стандартной библиотеки С/С++, вычислив среднее время работы обеих функции на следующих объемах данных: 
     1. 16 байт, 
     1. 700 байт, 
     1. 16 Кбайт, 
     1. 4Мбайта 
  * Количество повторений для каждого теста из п.1 **N=100**. Высчитать [среднее](https://ru.wikipedia.org/wiki/Математическое_ожидание) и [медиану](https://statanaliz.info/statistica/opisanie-dannyx/mediana-v-statistike/).
  * В качестве компиляторов для С/С++ использовать **GCC**, **Clang** или **ICC** (Intel C/C++ Compiler)
  * Можно использовать ассемблерные вставки или отдельные ассемблерные модули. 
  * Замеры проводить для 32-х битного и 64-х битного кода. 
  
  * При компиляции использовать оптимизацию. Например, для **GCC/ICC** нужно использовать следующие параметры:  
 ```
 -O2 -march=native -funroll-loops. 
 ```
  
  * **Требование:** реализованная функция должна работать не более чем на 10% медленнее в каждом тесте.  
