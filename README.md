<center> <img src=images/Booking.com_logo2.png> </center>


# <p style="border:5px solid Navy;text-align:center;font-size:100%;">Проект 3. Exploratory Data Analysis — разведывательный анализ данных</p>
<div class="alert alert-primary" role="alert">

##  Оглавление
1. [Описание проекта](#Описание-проекта)
2. [Описание данных](#Описание-данных)
3. [Зависимости](#Зависимости)
4. [Установка проекта](#Установка-проекта)
5. [Использование проекта](#Использование-проекта)
6. [Авторы](#Авторы)
7. [Выводы](Использование-проекта)



## <p style="border:5px solid Navy;text-align:center;font-size:100%;">Описание проекта</p>
<div class="alert alert-primary" role="alert">

> **Разведывательный анализ данных** — Exploratory Data Analysis. Этот этап дата-сайентисты проводят перед построением самой модели. 

Построение предсказательной модели обычно состоит из таких этапов: 
1. Формулировка бизнес-проблемы
2. Сбор данных и их очистка 
3. **Разведывательный анализ данных**
4. Разработка и построение модели
5. Внедрение модели в продакшен

Основные методы и алгоритмы разведовательного анализа показаны в данном проекте:
- FEATURE ENGINEERING (ПРОЕКТИРОВАНИЕ ПРИЗНАКОВ)
- FEATURE SELECTION (ОТБОР ПРИЗНАКОВ)
- КОДИРОВАНИЕ ПРИЗНАКОВ


**Цель Разведовательного Анализа Данных** — понять, что нам могут дать данные, и как признаки могут быть взаимосвязаны между собой. Понимание изначальных признаков позволяет создать новые, более сильные признаки и повысить качество модели. 



**Данный проект** направлен на демонстрацию применения различных методов и алгоритмов **Exploratory Data Analysis** на примере датасета с
соревнования на сайте **[kaggle](https://www.kaggle.com/competitions/sf-booking)**.

**О структуре проекта:**

* [images](./images) - папка с изображениями, необходимыми для проекта
* [project_3.ipynb](./data-cleaning.ipynb) - jupyter-ноутбук, содержащий основной код проекта, в котором демонстрируются методы и алгоритмы **Exploratory Data Analysis**. 
* [requirements.txt](./requirements.txt) - файл с зафиксированными версиями библиотек.



## <p style="border:5px solid Navy;text-align:center;font-size:100%;">Описание данных</p>
<div class="alert alert-primary" role="alert">

> **Постановка проблемы** — представьте, что вы работаете датасаентистом в компании Booking. Одна из проблем компании — это нечестные отели, которые накручивают себе рейтинг. 

> **Цель проекта** — построение модели, на основе алгоритмов машинного обучения, которая предсказывает рейтинг отеля.
    
> **Задачи проекта:** 
1. Принять участие в соревновании на платформе KAGGLE.COM
2. Выполнить подготовку данных, которые будут использованы для обучения модели
3. Изучить пример машинного обучения (scikitlearn класс RandomForsetRegressor)
4. Проверить эффективность предлагаемой модели, используя метрику MAPE

### Исходные данные представляют собой таблицу с информацией об отеле:

#### - **hotel_address** - адрес отеля
#### - **review_date** - дата, когда рецензент разместил соответствующий отзыв.
#### - **average_score** - средний балл отеля, рассчитанный на основе последнего комментария за последний год
#### - **hotel_name** - название отеля
#### - **reviewer_nationality** - национальность рецензента
#### - **negative_review** - отрицательный отзыв, который рецензент дал отелю.
#### - **review_total_negative_word_counts** - общее количество слов в отрицательном отзыв
#### - **positive_review** - положительный отзыв, который рецензент дал отелю
#### - **review_total_positive_word_counts** - общее количество слов в положительном отзыве
#### - **reviewer_score** - оценка, которую рецензент поставил отелю на основе своего опыта
#### - **total_number_of_reviews_reviewer_has_given** - количество отзывов, которые рецензенты дали в прошлом
#### - **total_number_of_reviews** - общее количество действительных отзывов об отеле
#### - **tags** - теги, которые рецензент дал отелю.
#### - **days_since_review** - продолжительность между датой проверки и датой очистки
#### - **additional_number_of_scoring** - есть также некоторые гости, которые просто поставили оценку сервису, а не оставили отзыв. Это число указывает, сколько там действительных оценок без проверки.
#### - **lat** - широта отеля
#### - **lng** - долгота отеля



Изначальные данные можно скачать **[здесь](https://www.kaggle.com/competitions/sf-booking/data)**.


Необходимо заранее создать папку **data** в директории, где лежит файл **project_3.ipynb**. Затем нужно сохранить файлы в формате **.csv**, скачанные по ссылкам предоставленным выше и положить эти файлы в папку **data**.


## Используемые зависимости
* Python (3.9):
    * [numpy (1.20.3)](https://numpy.org)
    * [pandas (1.3.4)](https://pandas.pydata.org)
    * [matplotlib (3.4.3)](https://matplotlib.org)
    * [seaborn (0.11.2)](https://seaborn.pydata.org)
    * [sklearn(1.2.2)](https://scikit-learn.org/stable/)
    

    

## Установка проекта

[git clone](https://github.com/galleydata/EDA.git)


## Использование
Вся информация о работе представлена в jupyter-ноутбуке project_3.ipynb.

## Авторы

* Ярослав Москаленко

## Выводы

1. Эксперементально убедился, что отбор признаков может сильно повлиять на конечный результат работы модели.
2. Не нашёл однозначного способа отбора признаков. Признаки с высокой корреляцией важны для работы модели и при их удалении приводят к ухудшению результатов метрики. Приходилось эксперементально определять признаки для удаления на этапе отбора признаков.
2. Для построения предсказательной модели наибольшее значение имеет анализ и обработка отзывов.
3. На практике воспользовалься несколькими методами и библиотеками для обработки отзывов.



  
