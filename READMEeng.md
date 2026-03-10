# AgroHub

RESTful API сервис для агро-платформы, объединяющей фермеров и покупателей.
Реализована ролевая модель (Фермер, Клиент), управление категориями и продуктами, оформление заказов и получение статистики фермерского магазина.

## Технологический стек
* **Язык:** Java 25
* **Фреймворк:** Spring Boot 4.0.3 (Web, Data JPA)
* **База данных:** PostgreSQL
* **Аутентификация:** JWT Токены
* **Инструменты:** Maven
* **Документация:** Swagger (Springdoc OpenAPI)

## Функционал
* **Аутентификация:** Регистрация и вход (выдача JWT токена).
* **Публичный доступ:** Просмотр списка продуктов, категорий, поиск по названиям.

* **Роль "FARMER":**
  * Управление своими категориями (создание, удаление).
  * Управление продуктами (добавление, удаление).
  * Просмотр заказов своего магазина.
  * Получение статистики (доходы, клиенты).
* **Роль "CLIENT":**
    * Оформление заказа.
    * Отмена заказов.

## Установка и запуск

Этот проект использует PostgreSQL. Перед запуском убедитесь, что у вас установлена и запущена база данных, а настройки подключения указаны в application.properties (или application.yml).

1.  **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/theaprilthreatwind/aitu-mvp-project.git
    cd aitu-mvp-project
    ```
2.  **Настройте базу данных PostgreSQL:**
    Создайте базу данных (например, agrohub) и обновите конфигурацию в src/main/resources/application.properties:
    ```bash
    spring.datasource.url=jdbc:postgresql://localhost:5432/agrohub
    spring.datasource.username=ваш_пользователь
    spring.datasource.password=ваш_пароль
    spring.jpa.hibernate.ddl-auto=update
    ```
3.  **Запустите приложение:**
    ```bash
    ./mvnw spring-boot:run
    ```

4. **Подключение доступа к фронтенду (весь мост с фронтендом выстроен через ngrok):**
    ```bash
    ngrok config add-authtoken <38DU12yBHRx4Jo34wRMlPxpFZP8_89xoDdkLsa2iec1G7PE2q>
    ngrok http 8080
   ```
   Скопируйте URL (например: https://unnegotiated-apocalyptically-paulette.ngrok-free.dev) и передайте его разработчикам фронтенда.

5. **API Документация Swagger:**
    После успешного запуска перейдите в браузере по адресу:
   https://unnegotiated-apocalyptically-paulette.ngrok-free.dev/swagger-ui/index.html (здесь можно протестировать все эндпоинты без сторонних программ).

**Автор:** Найданов Мирон