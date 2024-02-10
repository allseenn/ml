# Машинное обучение

## Данные

**Data science**- инструменты и подходы для работы с данными

**Big Data** - инструменты для работы с большими данными

**Dataset** - данные, набор объектов с признаками:
- train dataset - тренировочные (обучающие) данные
- test dataset - тестовые (проверочные) данные, для проверки качества обучения итоговой модели
- validation dataset - валидационные данные для подбора гипермараметров



**Feature** - Признак (возраст, пол, ЗП и т.д.)
- Первоначальные, содержащиеся в данных
- Вычисляемые по алгоритму
- Выделеннные самой программой
- Разметка (аннотация), часто используют в графике или видео

**Feature types** 
- binary (пол, да-нет)
- категориальные (Имена, Города, Болезнь и т.д), часто переводят в количественные для понимания алгоритмами
- Количественные (Длина, Ширины, Стоимость, Доля)
- Дата/Время (в моделях не используют в чистом виде)
- NaN - пропуски, пустые данные
**Object** - объект (наблюдения) исследования к которому относятся признаки (человек, пациент)

**Target (label)** - Целевой признак (возвращение кредита в срок)

**Design matrix** - Матрица исходных данных (матрица информации), это набор признаков без объектов


**Data types** - типы данных:
- Табличные
- Тексты
- Изображения
- Временные ряды (данные по одному показателю в течении времени)

**Data mining (source)**
- Открытые источники
- API
- Инструменты сбора собственных данных (аналитика сайта)
- Напрямую от изучаемого объекта

**Несбалансированные данные** - 5% кошек, 95% собак


## Алгоритмы МО

**Модель** - функция описывающая данные и значения всех весов

**Параметры модели** - параметры изменяются в процессе обучения

**Гиперпараметры модели** - параметры модели, которые не изменяются в процессе обучения

**Обученнная модель** = модель + параметры [+ гиперпараметры]

$$y = w_0 + w_1\cdot x_1 + w_2\cdot x_2 + w_n\cdot x_n$$

**loss function** - Функция потерь. оценивает ошибку между предсказанными значениями модели и истинными значениями целевой переменной в обучающем наборе данных

MSE (Mean Squared Error) и MAE (Mean Absolute Error) - это две распространенные метрики (меры) потерь, используемые в задачах регрессии. Они зависят от размерности целевой переменной (target). Обычно используются как **функции потерь**

**Градиентный спуск (Gradient Descent)** - метод для поиска минимума функции потерь, последовательным перебором значений и расчета их градиента

**Стохастического градиентного спуска (Stochastic Gradient Descent, SGD)** - метод, при котором вычисляются градиенты по одному или нескольким случайно выбранным образцам.

Главная идея градиентных спусков, что с помощью производной по весам ищем самую глубокую "впадину" функции.


### Обучение с учителем - labeled dataset 
Обучение с учителем предназначено для решения следующих задач:
1. классификации (определение спама, мошенников, болезней, грунта)
2. регрессии (прогноз погоды, прогноз цены, предсказание времени подачи такси)

#### 1. Алгоритмы для решения задач классификации

1. Логистическая регрессия
2. Наивный Байесовский алгоритм
3. Метод опорных вектором (SVD)
4. Алгоритмы, основанные на деревьях решений и их ансамблях
5. Нейронные сети

#### 2. Алгоритмы для решения задач регрессии

1. Линейная регрессия
2. Полиномиальная регрессия
3. Алгоритмы, основанные на деревьях решений и их ансамблях
4. Нейросети

### Обучение без учителя - unlabeled dataset

1. Кластеризация (сегментация пользователей, поиск аномалий, создание новых признаков для обучения с учителем, определение тематики текста)
2. Уменьшение размерности данных (уменьшаем количество признаков для анализа фейков, рекомендательные системы, поиск тематик похожих текстов, изучение клеток, создание новых признаков для обучения с учителем)

#### 1. Алгоритмы для решения задач кластеризации

1. Метод K-средних
2. DBSCAN
3. Mean Shift
4. EM-алгоритм
5. Методы иерархической кластеризации (родословные)
6. Нейронные сети

#### 2. Алгоритмы для решения задач по уменьшению данных

1. Метод главных компонентов (PCA)
2. CCA
3. t-SNE (визуализация)
Лингвистический анализ:
4. Латентное размещение Дирихле (LDA)
5. Латентно-семантический анализ (LSA, pLSA, GLSA)

### Обучение с подкреплением

похоже на обучение с учителем (только программа не получает сразу ответы, а вознаграждение или обратную связь): 

АГЕНТ -> действие <- вознаграждение <- наблюдение СРЕДА

Применяют для создания: автопилотов, игр, роботы-пылесосы, торговля на бирже, оптимизация предприятия

## Примеры МО

1. Торговля
2. Производство
3. Финансы
4. Добыча ископаемых
5. Транспорт и логистика
6. Тексты
7. Медицина

### 1. Рекомендательные системы в торговле

- Рекомендация фильмов- классификация
- Динамическое ценообразование (андроид, IOS) - классификация
- Анализ поведение покупателей - регрессия компьютерное зрение

### 2. Производство

- Определение вероятности поломки оборудования
- Оптимизация издержек - регрессия
- Контроль качества

### 3. Финансы

- Обнаружение мошеннических операций
- Прогнозирование ценных бумаг

### 4. Добыча ископаемых

- Анализ шума новых месторождений
- Анализ изображений горных пород

### 5. Транспорт и логистика

- Прогнозирование времени подачи такси
- Автопилоты

### 6. Тексты

- Автоматический перевод
- Чат и голосовые боты

### 7. Медицина

- Разработка лекарств (поиск мишени, ингибиторов, исследования)
- Персонифицированный подбор лекарств

## Оценка (метрики) модели МО

- выбор лучшего алгоритма для обработки данных
- избежать переобучения

**Переобучение модели** - переподгонка под обучающий датасет

Примеры переобучения - полиномиальная регрессия 

<2 40:50>

Оценки, с помощью которых можно улучшить предсказание:

**Variance** - Разброс, отличие между тем как модель работает на тренировочном и тестовом 

**Bias** - смещение, ошибка на тренировочном датасете 

<2 42:12>


### Оценки предсказаний регрессии

Вычисляем на сколько предсказанные значения отличаются от реальных

Меры (метрики)
1. средняя абсолютная ошибка MAE
2. средняя квадратичная ошибка MSE
3. коэффициент детерминации $R^2$


#### 1. MAE

Средняя абсолютная ошибка, наименьшее расстояние от значений обучающей выборки до варианта (функции) модели. Менее чувствительна к выбросам в распределении данных.

$$MAE = \frac{1}{n}\sum_{i=1}^n|Y_i-\hat Y_i|$$ 

<2 07:45>

- $Y_i$ - значений обучающей выборки
- $\hat Y_i$ - значение в модели
- n - количество точек

#### 2. MSE

Средняя квадратичная ошибка вычисляет среднее значение квадратов разностей между предсказанными значениями модели и истинными значениями целевой переменной. Более чувствительна к выбросам в распределении данных.

$$MAE = \frac{1}{n}\sum_{i=1}^n(Y_i-\hat Y_i)^2$$ 

#### 3. $R^2$

Коэффициент детерминации, показывает на сколько наша модель лучше, чем прямая, проходящая через среднее значение Y. Принимает значения от 0 до 1, чем ближе к 1 - тем модель лучше.
<2 50:25>

$$R^2=1-\frac{SS_{RES}}{SS_{TOT}} = 1-\frac{\sum_i(y_i-\hat y_i)^2}{\sum_i(y_i-\overline y)2}$$

### Оценки предсказаний классификации

Вычисляем сколько значений классов было предсказано правильно

Меры (метрики)
0. Матрица ошибок Матрица ошибок 
1. Доля верных ответов Accuracy
2. Полнота Recall
3. Точность Precision
4. F1-score
5. Оценка качества ROC AUC

#### 0. Confusion matrix 

Служит только для вычисления остальных метрик

<table boder=1>
<tr><td></td><td>1</td><td>0</td></tr>
<tr><td>1</td><td bgcolor=green>TP</td><td bgcolor=red>FP<br>ошибка 1 рода</td></tr>
<tr><td>0</td><td bgcolor=red>FN<br>ошибка 2 рода</td><td bgcolor=green>TN</td></tr>
</table>

#### 1. Accuracy

Доля верно предсказанных значений из всех (доля верных ответов)

$$Accuracy=\frac{TP+TN}{ALL}$$

#### 2. Recall

Доля верно предсказанных беременных из всех реально беременных (полнота, чувствительность)

$$Recall=\frac{TP}{TP+FN}$$

#### 3. Precision

Доля верно предсказанных беременных из тех, кто были предсказаны как беременные (точность)

$$Precision=\frac{TP}{TP+FP}$$

#### 4. F1-score

<2 54:13>

Гармоническое среднее для precision и recall

$$F1-score=\frac{2\cdot precision\cdot recall}{precision + recall}$$

#### 5. ROC AUC

- TPR=recall=чувствительность
- AUC-площадь под ROC-кривой
- $FPR=1-специфичность=\frac{FP}{FP+TN}$ 

<2 1:03:13>