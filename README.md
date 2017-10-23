# Laravel Chat API

Описание|Метод|Входные параметры
-|-|-
*Регистрация пользователя.* Регистрирует пользователя на сайте|`App\Http\Controllers\Auth\AuthController::create()`|Информация о пользователе
*Отправка сообщения.* Отправляет через socket.io в канал redis сообщение, переданное  во входные параметры|`App\Http\Controllers\ChatController::sendMessage()`|Сообщение
*Открытие чата.* В случае если пользователь авторизован данные метод открывает страницу чата с возможностью отправки сообщения|`App\Http\Controllers\HomeController::index()`|-

## Описание входных параметров

### Информация о пользователе

Массив вида:
```php
[
    'name'     => '<user_name>'
    'email'    => '<user_email>'
    'password' => '<password>'
]
```

### Сообщение

Массив вида:
```php
[
    'message' => '<message_text>'
    'user'    => '<user_name>'
]
