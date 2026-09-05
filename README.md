## About

GitHub Action, чтобы подключить раннер к инстансу Headscale. 

## Использование

### Быстрый старт

```yaml
name: Connect to Headscale

on:
  push:

jobs:
  connect:
    runs-on: ubuntu-latest
    steps:
      - name: Connect to Headscale tailnet
        uses: pluxa1221/headscale-action@v1
        with:
          login-server: '${{ secrets.HEADSCALE_URL }}'
          auth-key: '${{ secrets.TAILSCALE_AUTH_KEY }}'
```

## Кастомизация

### Входные данные

Следующие ключи могут быть использованы в блоке `step.with`:

| Название                          | Тип    | Описание                                              |
|-----------------------------------|--------|-------------------------------------------------------|
| `login-server`                    | String | URL вашего инстанса Headscale.                        |
| `auth-key`                        | String | Preauthkey для входа раннера в Tailnet автоматически. |

## Выход

Этот Github Action не предоставляет никакого выхода, кроме как подключения к Tailnet.

## License

Проект находится под лицензией MIT. Смотрите [LICENSE](LICENSE) для подробностей.
