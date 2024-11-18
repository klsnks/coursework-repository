### О проекте

Этот проект был выполнен в среде Google Colab. Вы можете ознакомиться с ним по следующей ссылке:
https://drive.google.com/drive/folders/1LLf6gLJ3O4BwzXG-F1Cj53iDvpcA_YbR?usp=sharing

## 0. Мотивация

<div style="text-align: justify; margin-left: 20px;"> Интеграция глубинного обучения в эконометрическое моделирование позволяет более точно учитывать асимметричные эффекты и нелинейности, которые возникают в ответ на монетарные шоки. Например, использование нейронных сетей в сочетании с методами локальных проекций (Local Projections) открывает новые возможности для изучения динамики временных рядов в условиях шоков различной интенсивности.</div>

## 1. Данные

<div style="text-align: justify; margin-left: 20px;"> Для сопоставимости результатов используются месячные данные по экономике США за 1988–2019 годы. Шок ДКП аппроксимируется через колебания цен финансовых активов в момент объявления решений, как предложено в [Bauer and Swanson(2023)]. Рассматриваются следующие макроэкономические показатели: промышленное производство, уровень безработицы и индекс потребительских цен, индекс цен на товары, премия за риск корпоративных облигаций, доходность 2-летних казначейских облигаций, ожидаемая инфляция на год вперёд. Основными источниками данных являются Федеральная резервная система США, Бюро статистики труда и информационная платформа Bloomberg.</div>

## 2. Методология

<div style="text-align: justify; margin-left: 20px;">Исследование основывается на модифицированной модели локальных проекций, которая традиционно используется для оценки импульсного отклика переменной y на шок e. Основное уравнение локальных проекций имеет вид:</div>

$$
\Delta y_{t+h} = \alpha_h + \beta_h^{\text{ols}} e_t + \delta_h X_t + \varepsilon_{t+h},
$$

где $$\Delta y_{t+h}\$$ — изменение переменной $$y$$ на горизонте $$h$$, $$e_t$$ — шок, $$X_t$$ — вектор контрольных переменных, $$\beta_h^{\text{ols}}$$ — коэффициент, описывающий линейный эффект шока, а $$\varepsilon_{t+h}$$ — случайная ошибка.

## 3. Результаты

