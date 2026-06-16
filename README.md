# Componenta HTTP PSR Nyholm

Nyholm PSR-7 and PSR-17 integration for Componenta HTTP. The package registers `Nyholm\Psr7\Factory\Psr17Factory` and aliases all standard PSR-17 factory interfaces to it.

## Installation

```bash
composer require componenta/http-psr componenta/http-psr-nyholm
```

## Registered Services

`Componenta\Http\Psr7\Nyholm\ConfigProvider` registers `Psr17Factory` and aliases:

- `RequestFactoryInterface`
- `ResponseFactoryInterface`
- `ServerRequestFactoryInterface`
- `StreamFactoryInterface`
- `UploadedFileFactoryInterface`
- `UriFactoryInterface`

## Boundary

This package only supplies factories. Server request creation is configured by `componenta/http-psr`, and response emission is handled by `componenta/http-emitter`.
