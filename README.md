Role Name
=========

Роль для установки vector.
- Установка vector
- Создание systemd unit Vector
- Конфигурирование vector на передачу данных в clickhouse

Requirements
------------

Role Variables
--------------

Переменные для установки кредов
default/main.yml:
```yaml
clickhouse_user: root
clickhouse_password: netology
```

Конфигурация для сбора и передачи логов содержится в vars/main.yml

Dependencies
------------

В `inventory` должен быть хост `clickhouse-01`
```yaml
endpoint: http://{{ hostvars['clickhouse-01'].ansible_host }}:8123
```

Требуется роль [clickhouse-role](https://github.com/danilabar/clickhouse-role)

Example Playbook
----------------

```yaml
hosts: vector
roles:
  - role: vector-role
```

License
-------

MIT

Author Information
------------------
