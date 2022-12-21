# BTC_bot with FastAPI
Учебный проет по реализации чат-бота в Телеграм для взаимодействия с кошельком биткоина.

#### В проекте реализованы следующие функции:
##### Для пользователя:
- получения информации о своем балансе и адресе кошелька
- перевод средств на другие кошельки в тестовой или основной сети
- получение информации о проведенных транзакциях

##### Для администратора:
- получение списка всех пользователей
- получение информации о пользователе
- удаления пользователя 
- получение общего баланса

##### При этом реализованы:
- инлайт-кнопки
- пагинация про просмотре списка пользователей администратором
- аутентификация OAuth2 c использования JWT - токена


#### Стек технологий:
Python3.10
PonyORM - база данных
Pydantic - для валидации данных
FastAPI - реализация API
TelegramBot - функционал чат-бота
Bit - взаимодействие с сетью Биткоин
Uvicorn - локальный сервер


#### Запуск приложения.

Создаем и запускаем локальное окружение:

python -m venv ENV 
source env/Scripts/activate

Установите зависимости из requirements.txt:

`pip install -r requirements.txt`

Настраиваем конфигурации приложения в файле config.py:

-Создаем посредством BotFather чат-бот и присваиваем его значения в переменную BOT_TOKEN
-Присваеваем Ваш ID в переменную TG_ADMIN_ID # сможем взаимодействовать с ботом как админ

Запускаем локальный сервер:

`uvicorn app:api --reload`

Ждем создания базы данных

Запускаем файл tg_bot.py
При этом база данных заполнителься пользователя, первый будет с Ваши ID в Телеграм

Через кнопку "Кошелек" Вы можете узнать адрес своего кошелька в сети.
Получител из биткоин-крана тестовые монеты и попробуйте их перевести, например, вернув обратно в тестовое хранилище




