
python-flask-docker

Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask Данные: с https://archive.ics.uci.edu/ml/datasets/Adult

Задача: предсказать по описанию вакансии является ли она фейком или нет (поле fraudulent). Бинарная классификация

Используемые признаки:

    education-num (float)
    age (float)
    hours-per-week (float)

Преобразования признаков: tfidf

Модель: logreg
Клонируем репозиторий и создаем образ

$ git clone https://github.com/myselfadmirer/Course_project_business_ML.git 
$ cd Course_project_business_ML 
$ docker build -t  .

Запускаем контейнер

Здесь хранится предобученная модель (/home/tamara/NELYUBINA/git-project/ML-in-business/lesson9/Course_project_business_ML/app/app)

$ docker run -d -p 8180:8180 -p 8181:8181 -v /home/tamara/NELYUBINA/git-project/ML-in-business/lesson9/Course_project_business_ML:/app/app/models fimochka/gb_docker_flask_example

Переходим на localhost:8181

