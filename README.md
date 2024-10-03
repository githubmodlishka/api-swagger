<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>API Swagger</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }
        h1, h2, h3 {
            color: #333;
        }
        code {
            background: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
        }
    </style>
</head>
<body>

<h1>API Swagger</h1>

<h2>Описание</h2>
<p>Этот API предназначен для получения Social Security Number (SSN) по данным пользователя. Он использует <strong>OAuth 2.0</strong> для авторизации и оптимизирован для высокой нагрузки, обеспечивая минимальную производительность в <strong>2 запроса в секунду</strong> для каждого эндпоинта.</p>

<h2>Возможности</h2>
<ul>
    <li><strong>Получение SSN</strong> по следующей информации:
        <ul>
            <li>Имя (firstname)</li>
            <li>Отчество (middlename)</li>
            <li>Фамилия (lastname)</li>
            <li>Адрес (address)</li>
            <li>Город (city)</li>
            <li>Почтовый индекс (zip)</li>
            <li>Дата рождения (dob) (необязательно)</li>
        </ul>
    </li>
    <li><strong>Тестовая авторизация</strong> с использованием тестового токена.</li>
    <li>Полная <strong>документация API</strong> с примерами запросов и ответов.</li>
    <li>Поддержка <strong>лимитирования запросов</strong>.</li>
    <li>Подробная информация об ошибках и статусах.</li>
</ul>

<h2>Установка</h2>

<h3>Требования</h3>
<ul>
    <li>Go 1.16 или выше</li>
    <li>Docker (для Swagger UI, если требуется)</li>
</ul>

<h3>Шаги установки</h3>
<ol>
    <li>Клонируйте репозиторий:
        <pre><code>git clone https://github.com/ваш_логин/api-swagger.git</code></pre>
    </li>
    <li>Перейдите в папку проекта:
        <pre><code>cd api-swagger</code></pre>
    </li>
    <li>Установите зависимости (если есть):
        <pre><code>go mod tidy</code></pre>
    </li>
    <li>Запустите сервер:
        <pre><code>go run main.go</code></pre>
    </li>
</ol>

<h2>Тестирование API</h2>
<p>Для тестирования API вы можете использовать инструменты, такие как <strong>Postman</strong> или <strong>cURL</strong>. Вот пример запроса:</p>
<pre><code>GET http://localhost:8080/test-request?token=Bearer%20test_token_123456&firstname=John&lastname=Doe&zip=12345</code></pre>

<h2>Документация</h2>
<p>Документация API доступна по следующему адресу:</p>
<pre><code>http://localhost:8080/swagger-ui/index.html</code></pre>

<h2>Ограничения</h2>
<ul>
    <li><strong>Лимит запросов</strong>: Максимум 1000 запросов в час на клиента.</li>
    <li><strong>Длина строк</strong>:
        <ul>
            <li>Имя: максимум 50 символов</li>
            <li>Отчество: максимум 50 символов</li>
            <li>Фамилия: максимум 50 символов</li>
            <li>Адрес: максимум 100 символов</li>
            <li>Город: максимум 50 символов</li>
            <li>Почтовый индекс: должен соответствовать шаблону 12345 или 12345-6789</li>
        </ul>
    </li>
</ul>

<h2>Лицензия</h2>
<p>Этот проект лицензирован под <a href="LICENSE">MIT License</a>.</p>

<h2>Контакты</h2>
<p>Если у вас есть вопросы или предложения, вы можете связаться с нами по электронной почте: <strong>ваша почта</strong>.</p>

<hr>
<p>Спасибо за использование нашего API! Мы надеемся, что он будет полезен для вас.</p>

</body>
</html>
