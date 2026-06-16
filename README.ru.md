# Componenta HTTP PSR Nyholm

Интеграция Nyholm PSR-7 и PSR-17 для Componenta HTTP. Пакет регистрирует `Nyholm\Psr7\Factory\Psr17Factory` и назначает на него все стандартные интерфейсы PSR-17 фабрик.

## Установка

```bash
composer require componenta/http-psr componenta/http-psr-nyholm
```

## Что регистрирует пакет

`Componenta\Http\Psr7\Nyholm\ConfigProvider` регистрирует `Psr17Factory` и псевдонимы:

- `RequestFactoryInterface`
- `ResponseFactoryInterface`
- `ServerRequestFactoryInterface`
- `StreamFactoryInterface`
- `UploadedFileFactoryInterface`
- `UriFactoryInterface`

## Граница пакета

Пакет только предоставляет фабрики. Создание серверного запроса настраивает `componenta/http-psr`, а отправку ответа выполняет `componenta/http-emitter`.
