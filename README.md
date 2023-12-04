# DA-in-GameDev-lab5

Отчет по лабораторной работе #5 выполнил(а):
- Куплевацкий Денис Игоревич
- РИ220931

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
  
- Цель работы

- Задание 1. Найти внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели.

- Задание 2. Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.
  
- Задание 3. Приведите примеры, для каких игровых задач и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения?
  
- Выводы.

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1
### Найти внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели.
 
Ход работы: 
- В ходе выполнения первого задания из лабораторной работы №5 я создал сцену в Unity и реализовал систему поиска объекта агентом. Для этого я создал скрипт RollerAgent и добавил код, полученный из материалов лабораторной работы (https://drive.google.com/file/d/1vkf41XpFz8_E_reSRfKgCPDFfh_WZsX4/view).
- В контексте машинного обучения коэффициент корреляции обычно используется для измерения степени линейной зависимости между двумя переменными. Этот коэффициент может помочь определить, насколько изменения в одной переменной связаны с изменениями в другой переменной. В машинном обучении коэффициент корреляции может быть полезен для анализа данных и понимания взаимосвязей между признаками.
- В данном скрипте нет конкретного коэффициента корреляции, согласно определению. Однако, в текущем контексте, его роль может выполнять коэффициент "1.42f" в условной конструкции "if (distanceToTarget < 1.42f)".
- Переменная "distanceToTarget" является связью между агентом и целью агента, а коэффициент "1.42" является верхней границей этой переменной, влияющей на ход обучения объекта текущей задаче.
- ![image](https://github.com/parallaxD/DA-in-GameDev-lab5/assets/81700733/58e7c11d-6b63-4ba0-b570-2bd4807b5633)
- Переменная distanceToTarget в этом коде представляет собой расстояние между текущей позицией объекта (this.transform.localPosition) и целевой позицией (Target.localPosition).
- Если объект агента достигает цели (расстояние меньше 1.42f), то цель достигнута успешно, и агент получает вознаграждение. В противном случае, если агент опускается ниже определенной высоты (this.transform.localPosition.y < 0), эпизод также завершается, но без предоставления вознаграждения.
- **Вывод о его влиянии на обучение следующий:** чем меньше этот коэффициент, тем точнее будет обучаться модель, ведь расстояние, необходимое для получения вознаграждения, будет меньше. Соответственно, чем он больше, тем менее точно происходит обучение. Необходимо отметить, что значение этого коэффициента также влияет на время обучения агента (обратно-пропорциональная зависимость).






## Выводы

В ходе лабораторной работы я пробовал обучать однослойный перцептрон некоторым логическим операциям (OR, AND, NAND, XOR). С первыми тремя всё прошло успешно, а с XOR перцептрон "не справился". (XOR-проблема, описанная Minsky)

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
