Инструкция по запуску (не закрывать вновь открытые вкладки):
docker compose up -d

Перейти на http://localhost:15101/swagger/index.html и зарегистрировать пользователя в POST /users

Через POST в /auth/login заходим и получаем JWT-токен (запоминаем)

Перейти на http://localhost:15103/swagger/index.html и зарегистрировать продукт в POST /products

Перейти на http://localhost:15102/swagger/index.html и зарегистировать заказ в POST /orders (нужен UserId)

На той же вкладке добавляем в PATCH /orders/{id}/items/add/ продукт в наш заказ (нужен OrderId, ProductId)

Перейти на http://localhost:15000/swagger/index.html и авторизироваться через кнопку Authorize, заполняем JWT-токен из шага 3

Загрузить через GET /api/profile/{userId} информацию (заказы и личная информация) о пользователе (нужен UserId)
