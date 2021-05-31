
python-flask-docker

Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask Данные: с https://archive.ics.uci.edu/ml/datasets/Adult

Данные из базы переписи 1994 года. 
Задача прогноза - определить, зарабатывает ли человек более 50 тысяч в год.

Целевая переменная: 
target: более 50 тыс - >50K, менее или равно 50 тыс - <=50K. Бинарная классификация

Используемые признаки:

    education-num (float)
    age (float)
    hours-per-week (float)
    capital-gain (float)

Преобразования признаков: OHEEncoder. StandardScaler

Модель: GradientBoostingClassifier
Клонируем репозиторий и создаем образ

    $ git clone https://github.com/myselfadmirer/Course_project_business_ML.git 
    $ cd Course_project_business_ML 
    $ docker build -t  myselfadmirer/Course_project_business_ML 

Запускаем контейнер

Здесь хранится предобученная модель (/home/tamara/NELYUBINA/git-project/ML-in-business/lesson9/Course_project_business_ML/app/models)

$ docker run -d -p 8180:8180 -p 8181:8181 -v /home/tamara/NELYUBINA/git-project/ML-in-business/lesson9/Course_project_business_ML:/app/models  myselfadmirer/Course_project_business_ML

Переходим на localhost:8181
