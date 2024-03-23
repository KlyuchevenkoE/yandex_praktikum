# Применение методов машинного обучения для выбора локации бурения скважин

[ipynb](https://github.com/KlyuchevenkoE/yandex_praktikum/blob/master/notebooks/7_ml_business_oil/ml_business_oil.ipynb)

## Описание проекта

Нужно решить, где бурить новую скважину для добывающей компании. Предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. Построим модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Проанализируем возможную прибыль и риски техникой Bootstrap.

## Навыки и инструменты

- **python**
- **pandas**
- **pandas_profiling**
- **seaborn**
- **numpy**
- **matplotlib**
- **stats**
- sklearn.model_selection.**KFold**
- sklearn.utils.**shuffle**
- sklearn.metrics.**mean_squared_error**
- sklearn.linear_model.**LinearRegression**
- sklearn.preprocessing.**StandardScaler**

## 

## Общий вывод

Не смотря на низкие показатели средней выручки и объемов добычи при обучении модели, второй регион показывает лучий результат при оценке рисков:

* 2,5% квантиль только во вторм регионе превышает нулевой порог, причем на 15 миллионов
* При этом оценка дает здесь наивысший показатель средней выручки с наименьшей дисперсией
* Также риск убытков у регина под номером два всего 0,3% в сравнении с 6% у 1 и 3 претендентов
Для разработки выбираем второй регион (geo_data_1.csv)