<span style="color:#660099">
<h1>Предсказание цены автомобиля</h1></span>

***Cферы деятельности компании:***

- Ритейл / E-commerce
- Площадки объявлений
- Интернет-магазины
- Отраслевые компании / Индустрия / Промышленность
- Услуги для бизнеса [b2b]
- Стартапы
- IT-компания
    
***Задачи проекта:***

Обучить модель для определения рыночной стоимости автомобиля

***Описание проекта:***
    
Сервис по продаже автомобилей с пробегом разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. 
Проанализированы данные: технические характеристики, комплектации и цены автомобилей. Построена модель для определения стоимости автомобиля с пробегом.
Использованы численные методы, приближённые вычисления, оценка сложности алгоритма, градиентный спуск.

***Навыки и инструменты:***

предобработка данных, python, pandas, numpy, re, seaborn, matplotlib, sklearn, catboost, lightgbm, timeit	

***Вывод:***

- Были подобраны гиперпараметры и обучены 6 различных моделей.
- Все модели прошли проверку на вменяемость в сравнении с моделью DummyRegressor, которая предсказывала всегда среднюю стоимость автомобиля. В итоге все модели были протестированы.
- У линейных моделей единственственное преимущество перед остальными моделями (кроме дерева решений) - у них очень быстрая скорость предсказания, но качество так же как и на обучающей выборке хуже остальных. 
- Дерево решений - середнячок по качеству предсказаний и лучшая модель по скорости предсказания.
- Значительно лучше остальных по качеству предсказания справились с задачей модели  с использованием градиентного бустинга. Модели CatBoostRegressor и LGBMRegressor показали примероно одинковое качество по значению метрики RMSE - при определении стоимости автомобиля они в среденем ошибаются на 1500 евро. Но стоит отметить что обе модели не исчерпали свой потенциал, так как большая часть гиперпараметров не была задействована в переборе, а значит метрику качества можно улучшать.