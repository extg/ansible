# Ansible Toolkit

Коллекция ролей для быстрой настройки vps под разные цели.

* `bootstrap.yml` - подготовка vsp для дольнейшего деплоя (установка python и locales)
* `inventory/hosts` - список хостов и данные для подключения к ним.

## Roles

* `nginx`
* `php`
* `git`
* `mysql`
* `opencart`
* `node`

## Quick start

1. Укажите данные для подключения в `inventory/hosts`
2. Укажите в `boostrap.yml` в задаче `Install base utilities` какие вам нужны предустановленные
  пакеты на сервере (не указывайте, то что устанавливается через роли)
3. Выполните `ansible-playbook -i inventory/hosts bootstrap.yml` для первоначльной настройки сервера
4. Укажите нужные вам роли и параметры в  `site-*.yml`
5. Запустите `ansible-playbook -i inventory/hosts site-*.yml`
