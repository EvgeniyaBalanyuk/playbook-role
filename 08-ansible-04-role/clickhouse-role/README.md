# ClickHouse Role

## Описание

Роль `clickhouse-role` предназначена для установки и настройки ClickHouse на целевых серверах. Она автоматически загружает необходимые пакеты, устанавливает их, запускает сервис ClickHouse и создает базу данных `logs`.

## Требования

- Ansible версии 2.9 или выше
- Целевая система: CentOS/RHEL 7 и выше, Fedora

## Зависимости

Нет внешних зависимостей.

## Переменные

### Дефолтные переменные (`defaults/main.yml`)

```yaml
# Версия ClickHouse для установки
clickhouse_version: "21.8.10.19"

# Список пакетов ClickHouse для установки
clickhouse_packages:
  - clickhouse-common-static
  - clickhouse-client
  - clickhouse-server
