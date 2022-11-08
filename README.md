
# <center>Real Estate Evaluation</center>

В настоящем задании, вы получаете доступ к набору данных о стоимости недвижимости в различных районах штата Калифорния, США. 

Данные хранятся в реляционной БД в виде двух таблиц:

**neighborhoods** - случайная выборка районов штата Калифорния. Каждая строка таблицы представляет собой какой-то район, имеющий такие атрибуты, как:

    - id - уникальный идентификатор, primary key;
    - longitude - географическая долгота, град.;
    - latitude - географическая широта, град.;
    - median_house_value - медианная стоимость жилого дома в данном районе, доллар США;
    - population - численность населения района, чел.;
    - ocean_proximity - кластер по принципу близости к океану, качественная переменная;
    
**cluster_mean_values** - каждая строка данной таблицы представляет собой кластер районов, сгруппированных по принципу близости к океану. Атрибуты:
    
    - ocean_proximity_cluster - кластер по принципу близости к океану, качественная переменная;
    - mean_median_house_value - среднее значение медианной стоимости жилого дома во ВСЕХ районах данного кластера, доллар США;
    
**ОБРАТИТЕ ВНИМАНИЕ**: **mean_median_house_value** - значение для всей генеральной совокупности районов в кластере. Таблица **neighborhoods**, в свою очередь, содержит только ВЫОБРКИ из каждого кластера, но не ген. совокупности. Если вы посчитаете среднее арифметическое **median_house_value** - это будет ВЫБОРОЧНЫМ значением.
***************************************
  
  
**ВАШИ ЗАДАЧИ:**

1) Извлечь таблицу **neighborhoods** в датафрейм. В части записей отсутствуют данные в атрибуте **ocean_proximity** (null-значения), их необходимо восстановить. Фактически, это задача классификации. Проведите разведочный анализ, подумайте, как в принципе её возможно решить;
    
2) Исправить null-значения **ocean_proximity** в самой БД. Условие: нельзя заменять таблицу в БД на новую, только через обновление значений с помощью SQL;
    
3) С помощью SQL создать объединенный датасет со значениями из двух таблиц БД, т.е. чтобы у каждого района было известно среднее арифметическое медианной стоимости жилья для районов в его кластере. Условие: только с помощью SQL, не с помощью Python; 
    
4) Определить форму распределения **median_house_value** в каждом кластере. Определить выборочные средние **median_house_value** и их отклонения от средних ген. совокупностей. Все изобразить графически для каждого кластера. В виде комментария описать ваши выводы о репрезентативности выборок;
В настоящем задании, вы получаете доступ к набору данных о стоимости недвижимости в различных районах штата Калифорния, США. 

Данные хранятся в реляционной БД в виде двух таблиц:

**neighborhoods** - случайная выборка районов штата Калифорния. Каждая строка таблицы представляет собой какой-то район, имеющий такие атрибуты, как:

    - id - уникальный идентификатор, primary key;
    - longitude - географическая долгота, град.;
    - latitude - географическая широта, град.;
    - median_house_value - медианная стоимость жилого дома в данном районе, доллар США;
    - population - численность населения района, чел.;
    - ocean_proximity - кластер по принципу близости к океану, качественная переменная;
    
**cluster_mean_values** - каждая строка данной таблицы представляет собой кластер районов, сгруппированных по принципу близости к океану. Атрибуты:
    
    - ocean_proximity_cluster - кластер по принципу близости к океану, качественная переменная;
    - mean_median_house_value - среднее значение медианной стоимости жилого дома во ВСЕХ районах данного кластера, доллар США;
    
**ОБРАТИТЕ ВНИМАНИЕ**: **mean_median_house_value** - значение для всей генеральной совокупности районов в кластере. Таблица **neighborhoods**, в свою очередь, содержит только ВЫОБРКИ из каждого кластера, но не ген. совокупности. Если вы посчитаете среднее арифметическое **median_house_value** - это будет ВЫБОРОЧНЫМ значением.
***************************************
  
  
**ВАШИ ЗАДАЧИ:**

1) Извлечь таблицу **neighborhoods** в датафрейм. В части записей отсутствуют данные в атрибуте **ocean_proximity** (null-значения), их необходимо восстановить. Фактически, это задача классификации. Проведите разведочный анализ, подумайте, как в принципе её возможно решить;
    
2) Исправить null-значения **ocean_proximity** в самой БД. Условие: нельзя заменять таблицу в БД на новую, только через обновление значений с помощью SQL;
    
3) С помощью SQL создать объединенный датасет со значениями из двух таблиц БД, т.е. чтобы у каждого района было известно среднее арифметическое медианной стоимости жилья для районов в его кластере. Условие: только с помощью SQL, не с помощью Python; 
    
4) Определить форму распределения **median_house_value** в каждом кластере. Определить выборочные средние **median_house_value** и их отклонения от средних ген. совокупностей. Все изобразить графически для каждого кластера. В виде комментария описать ваши выводы о репрезентативности выборок;
    
5) Определить зависимость стоимости жилья от численности населения района в каждом кластере. Описать в виде комментария;

P.S. Каждое задание необходимо сопроводить комментариями, в которых вы поясняете, чего конкретно добиваетесь и почему используете именно выбранный способ решения. Обоснуйте ваши действия и сформулируйте выводы.