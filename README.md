# blockchain-api-tg
Вводная:
1. Есть онлайн сервис https://flipsidecrypto.xyz, специализиующийся на хранении в реляционной базе данных данных из нескольких блокчейн-сетей. В основном это EVM сети
2. Данный сервис позволяет обращаться к этим данным с помощью SQL-интерфейса
3. У этого сервиса есть API для питона, позволяющий из питон кода запускать SQL запрос и получать на выходе JSON файл

Постановка задачи:
1. Написать телеграмм бота для работы с API сервиса flipsidecrypto
2. Бот должен принимать на вход от пользователя SQL запрос и возвращать данные в выбранном пользователем формате:
  а) В виде csv файла
  б) В виде графика (рисуем питоном график и отправляем пользователю картинкой)
3. Необходимо реализовать базовую проверку SQL запроса от пользователя. Тут есть несколько этапов проверки (пока на этапе ресерча):
  а) Проверка на существование таблиц и столбцов в базе данных
  б) Проверка синтаксиса запроса
  в) Поднять локально Postgres в Docker, положить туда тестовые сэмплы данных и протестировать выполнение запроса (опционально)
