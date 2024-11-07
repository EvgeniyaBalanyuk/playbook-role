# Vector Role

## Описание

Роль `vector-role` предназначена для установки и настройки Vector — инструмента для обработки, форматирования и передачи логов. Роль загружает дистрибутив Vector, устанавливает его и настраивает автозапуск сервиса.

## Поддерживаемые платформы

- Linux (поддерживаются большинство дистрибутивов)


## Пример использования

```yaml
- hosts: vector_servers
  roles:
    - role: vector-role
      vector_version: "0.16.1"
      vector_install_dir: "/opt/vector"
      vector_config_path: "/etc/vector/custom_vector.toml"