**Деплой docker-compose c помощью ansible-playbook**

_Версия ansible 2.8 (в идущей по умолчанию 2.0.0.2 нет модуля для работы с docker)_

1) Общая часть для двух вариантов: `ansible-playbook docker_install.yml` 
устанавливает docker, docker-compose и дополнительный софт для работы модуля docker_compose ansible

2) Первый вариант: `ansible-playbook docker-provision.yml` копирует файлы проекта docker-compose в удаленный каталог, проверяет текущий статус проекта docker-compose, собирает и запускает проект, проверяет стату запуска проекта. Используется файл docker-compose.yml

3) Второй вариант: `ansible-playbook docker-provision_builtin.yml` копирует файлы проекта в удаленный каталог, собирает проект, запускает проект и проверяет его статус запуска. Структура docker-compose.yml описана непосредственно в файле плейбука ansible.

4) `задача.yml` - решение текстовой задачи с вебинара.