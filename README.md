# semester-project-b-tree

_Краткое описание семестрового проекта._

- Реализуется b-tree (не путать с binary-tree)
- Является сбалансированным, сильно ветвистым деревом, все листья которого находятся на одной высоте
- Используется для работы с дисковой памятью и с базами данных
- Можно выполнять добавление, удаление и поиск
- Поиск, добавление и удаление в среднем за `O(log(n))`

## Команда "Ferenets boys"

Группа: 11-101

**Примечание**. Преподаватель может определить вклад любого из участников команды по истории коммитов.

| Фамилия Имя         | Вклад (%) | Прозвище              |
| :---                |   ---:    |  ---:                 |
| Хабибуллин Алишер   | 33        |  _Моргенштерн_        |
| Ловчицкий Михаил    | 33        |  _Бен_                |
| Насыров Азат        | 33        |  _зхцГуль_            |

**Девиз команды**
> _Наши цели ясны. Задачи определены. За работу, товарищи!_
## Структура проекта

_Описание основных частей семестрового проекта._
 Проект состоит из следующих частей:
- [`src`](src)/[`dataStructure`](dataStructure) - реализация структуры данных (исходный код и заголовочные файлы);
- [`src`](src)/[`benchmark`](benchmark) - контрольные тесты производительности структуры данных (операции добавления, удаления,
  поиска и пр.);
-[`src`](src)/[`dataset`](dataset) - генерация набора данных для тестов;
- [`dataset`](dataset) - наборы данных для запуска контрольных тестов;


**Пример**. Рекомендуемые требования:

1. Java-8 компилятор
2 Рекомендуемый объем оперативной памяти - не менее 8 ГБ.
3 Свободное дисковое пространство объемом ~ 2 ГБ (для входного набора данных).

## Сборка и запуск

### Пример (Windows)

#### Сборка проекта

_Опишите процесс сборки проекта._

Склонируйте проект к себе на устройство через [Git for Windows](https://gitforwindows.org/) (либо используйте
возможности среды разработки):

```shell
git clone https://github.com/Algorithms-and-Data-Structures-2022/semester-project-b-tree.git
```

Сборка и запуск проекта осуществляется через среду разработки.

#### Генерация тестовых данных

Формат данных: [text file(txt)](https://en.wikipedia.org/wiki/Text_file.)

Инструкции по генерации:
```shell
# переход в папку генерации набора данных
cd dataset
# компиляция и запуск java файла:
javac GenerateInput.java && java GenerateInput
```

По названию директории `/dataset/methodsData` можно понять, что здесь хранятся наборы данных для контрольных тестов по
**добавлению** элементов в структуру данных. Названия файлов `100.csv`. `5000000.csv` и т.д. хранят информацию о размере набора данных (т.е. количество элементов). 
В каждом наборе хранятся числа от 1 до 10*i, где i - порядковый номер набора

#### Контрольные тесты (benchmarks)

**Примечание**. Во избежание "захламления" репозитория большим объёмом данных рекомендуется указать ссылку на архив с
набором данных, который при необходимости можно скачать по ссылке. [Google Drive](https://google.com

##### Список контрольных тестов

| Название                  | Описание                                | Метрики         |
| :---                      | ---                                     | :---            |
|`Metrics`                  | поиск,удаление и добавление элементов   |_Время_          |

##### Примеры запуска

```shell
javac Metrics.java && java Metric <input> <output> <command> <set> <iterations>
```

- `<input>` - путь до входного файла  с набором данных в формате txt
- `<output>` -путь до выходного файла с результатами контрольного теста;
- `<command>` - название комманды которую необходимо протестировать;
- `<set>`- порядковый номер набора данных;
- `<iterations>` - количество повторений тестов

## Источники

_Список использованных при реализации структуры данных источников._

[Хабр](https://habr.com/ru/post/114154/);
[Хабр](https://habr.com/ru/post/337594/);
[YouTube](https://www.youtube.com/watch?v=WXXetwePSRk);
