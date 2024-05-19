LangTrainer - тренажер для изучения английского языка с использованием Anki-подобных карточек

Функциональность сервиса:

Создание карточки
Просмотр карточки с возможностью выбора верного ответа

Запуск сервиса:

1. Установить виртуальное окружение
2. Для windows - python -m venv myenv, myenv\Scripts\activate
3. Для macos/linux - python3 -m venv myenv, source myenv/bin/activate
4. Установить зависимости - pip install -r requirements.txt
5. Применить миграции - python3 manage.py migrate
6. Создать админа - python3 manage.py createsuperuser
7. Запустить сервер - python3 managep.py runserver
8. Варианты очистки id объектов (так мы сможем избежать ошибок при удалении созданной карточки):

delete from question_card; delete from sqlite_sequence where name='your_table';
SELECT setval('question_card_id_seq', <твое значение>, true); следующим будет id со значением <твое значение> + 1
