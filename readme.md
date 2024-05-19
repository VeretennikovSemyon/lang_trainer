LangTrainer - тренажер для изучения английского языка с использованием Anki-подобных карточек

Функциональность сервиса:
1. Создание карточки
2. Просмотр карточки с возможностью выбора верного ответа

Запуск сервиса:
1. Установить виртуальное окружение
2. Для windows - python -m venv myenv, myenv\Scripts\activate
3. Для macos/linux - python3 -m venv myenv, source myenv/bin/activate
4. Установить зависимости - pip install -r requirements.txt
5. Создать админа - python3 manage.py createsuperuser
6. Применить миграции - python3 manage.py migrate
7. Запустить сервер - python3 managep.py runserver

Варианты очистки id объектов (так мы сможем избежать ошибок при удалении созданной карточки):
1. delete from question_card; delete from sqlite_sequence where name='your_table';
2. SELECT setval('question_card_id_seq', <твое значение>, true); следующим будет id со значением <твое значение> + 1
