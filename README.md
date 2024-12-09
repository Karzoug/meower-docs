# Meower app

Микросервисное приложение социальной сети для публикации и взаимодействия с короткими сообщениями. 

Основные [сценарии использования](scenarios/), внутренние и внешние [интерфейсы](https://github.com/Karzoug/meower-api) (api).

Состоит из основных сервисов:
- [пользователей](https://github.com/Karzoug/meower-user-service)
- [сообщений](https://github.com/Karzoug/meower-post-service)
- [связей пользователей](https://github.com/Karzoug/meower-relation-service)
- [ленты пользователя](https://github.com/Karzoug/meower-timeline-service)
- [backend for web frontend](https://github.com/Karzoug/meower-web-service)

Все сервисы импортируют репозиторий [общего кода](https://github.com/Karzoug/meower-common-go) для приложения.

Также использует дополнительные сервисы, реализующие в основном экспорт в kafka или преобразование ее сообщений - они могут быть заменены на debezium или аналоги.
- [user-outbox](https://github.com/Karzoug/meower-user-outbox)
- [post-outbox](https://github.com/Karzoug/meower-post-outbox)
- [timeline-pipeline](https://github.com/Karzoug/meower-timeline-pipeline)