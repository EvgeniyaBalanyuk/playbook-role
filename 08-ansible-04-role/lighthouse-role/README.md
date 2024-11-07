# Ansible Role: lighthouse-role

Эта роль устанавливает и настраивает Lighthouse на хостах, указанных в инвентори.

## Требования

Поддерживается на системах с пакетом менеджером `yum`.

## Параметры

### Основные параметры (defaults/main.yml)

- `lighthouse_version` (по умолчанию: `"1.0.0"`) - Версия Lighthouse для установки.
- `lighthouse_package` (по умолчанию: `"lighthouse"`) - Имя пакета Lighthouse для скачивания.
- `lighthouse_url` (по умолчанию: `"https://packages.lighthouse.com/rpm/stable"`) - Базовый URL для скачивания пакетов.

### Дополнительные параметры (vars/main.yml)

- `lighthouse_config_path` - Путь к конфигурационному файлу Lighthouse.

## Задачи роли

- **Скачивание пакета**: Загружает пакет Lighthouse с указанного URL.
- **Установка пакета**: Устанавливает пакет на сервер.
- **Настройка конфигурации**: Генерирует конфигурационный файл на основе шаблона.
- **Управление службой**: Запускает и перезапускает сервис Lighthouse.

## Использование

Пример использования в плейбуке:

```yaml
- name: Install and configure Lighthouse
  hosts: lighthouse
  roles:
    - lighthouse-role
