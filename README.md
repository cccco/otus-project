# otus-project
Требования к реализации:

— Ansible-роли для развёртывания (под Vagrant, реальные сервера)

— Vagrant-стенд

В итоге в проект должны быть включены:
— как минимум 2 узла с СУБД; 

— минимум 2 узла с веб-серверами; 

— настройка межсетевого экрана (запрещено всё, что не разрешено); 

— скрипты резервного копирования; 

— центральный сервер сбора логов (Rsyslog/Journald/ELK). 

# Работоспособность

Поднимаем кластер `vagrant up && ansible-playbook cluster.yml`

Пробросим порт 80 c proxy1 на на домашнюю ОС `sudo ssh -N -L 8080:192.168.10.100:80 vagrant@127.0.0.1 -p 2222`

Перейдем по ссылке для и откроем установщик [wordpress](http://127.0.0.1:8080)
