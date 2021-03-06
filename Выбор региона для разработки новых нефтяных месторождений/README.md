## Проект. Выбор региона для разработки новых нефтяных месторождений. 
### Описание проекта
Для добывающей компании «ГлавРосГосНефть» нужно решить, где бурить новую скважину.

Предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. Необходимо построить модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Проанализировать возможную прибыль и риски техникой *Bootstrap.*

#### Шаги для выбора локации:

- В избранном регионе ищут месторождения, для каждого определяют значения признаков;
- Строят модель и оценивают объём запасов;
- Выбирают месторождения с самым высокими оценками значений. Количество месторождений зависит от бюджета компании и стоимости разработки одной скважины;
- Прибыль равна суммарной прибыли отобранных месторождений.

#### Условия задачи:
 - Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).
 - При разведке региона проводится исследование 500 точек.
 - Бюджет на разработку месторождений — 10 млрд рублей, стоимость бурения одной скважины — 50 млн рублей.
 - Один баррель сырья приносит 4500 рублей прибыли.
 - Не рассматривать регионы, в которых риск убытков выше 2.5%. Из оставшихся выбирается регион с наибольшей средней прибылью.

### Содержание проекта
1. Изучение общей информации о данных  
2. Обучение модели для каждого региона:  
  2.1. Разбить данные на обучающую и валидационную выборки в соотношении 75:25.  
  2.2. Обучить модель и сделайть предсказания на валидационной выборке.  
  2.3. Сохраниье предсказания и правильные ответы на валидационной выборке.  
  2.4. Напечатать на экране средний запас предсказанного сырья и RMSE модели.  
  2.5. Проанализируйте результаты.  
3. Подготовка к расчёту прибыли:  
  3.1. Все ключевые значения для расчётов сохранить в отдельных переменных.  
  3.2. Рассчитайте достаточный объём сырья для безубыточной разработки новой скважины. Сравните полученный объём сырья со средним запасом в каждом регионе.  
4. Написание функцию для расчёта прибыли по выбранным скважинам и предсказаниям модели:  
  4.1. Выберить скважины с максимальными значениями предсказаний.  
  4.2. Просуммировать целевое значение объёма сырья, соответствующее этим предсказаниям.  
  4.3. Рассчитать прибыль для полученного объёма сырья.  
5. Посчитаnm риски и прибыль для каждого региона:  
  5.1. Применить технику Bootstrap с 1000 выборок, чтобы найти распределение прибыли.  
  5.2. Найти среднюю прибыль, 95%-й доверительный интервал и риск убытков.  
  5.3. Предложить регион для разработки скважин.  
  
  ### Библиотеки, используемые в проекте:
- Pandas
- Numpy
- Scipy
- SKlearn


