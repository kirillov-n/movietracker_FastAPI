# FastAPI бэкенд сервиса по трекингу фильмов

## Запуск проекта
1) Разверните БД PostgreSQL (локально или докер-контейнер)

2) Склонируйте проект
   ```
   git clone https://github.com/kirillov-n/movietracker_FastAPI.git
   ```

3) Добавьте переменную окружения
   ```
   set PYTHONPATH=ССЫЛКА_НА_ПРОЕКТ
   ```

4) Создайте в корне проекта .env файл (рядом с requirements.txt) и замените значения на свои:
    ```
    # Переменные, связанные с БД
    DB_HOST='localhost'
    DB_PORT=5432
    DB_USER=<ИМЯ_ПОЛЬЗОВАТЕЛЯ>
    DB_PASS=<ПАРОЛЬ>
    DB_NAME=<НАЗВАНИЕ_БД>
    
    # Секретный ключ.
    SECRET='super_secret_key'
    ```

5) Создайте и активируйте виртуальное окружение:
    ```
   python -m venv venv
   venv\Scripts\activate.bat
    ```

6) Установите зависимости
    ```
   pip install -r requirements.txt
    ```

7) Запустите сервис:
    ```
   python ./src/main.py
    ```

8) Наполните таблицу films фильмами:
    ```
   python ./src/data/populate_films.py
    ```

9) Сервис доступен по адресу:
    ```
    http://localhost:8000
    ```

10) Если вам нужен другой адрес вы можете изменить его в main файле или запустить сервис командой (изменив значения):
    ```
    uvicorn src.app.app:app --host 127.0.0.1 --port 8000 --reload
    ```
