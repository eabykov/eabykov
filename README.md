Порядок изучения технологий для DevOps: https://roadmap.sh/devops (синими глочками рекомендуемое к изучению, зелеными алтернативный вариант и серыми не обязательное)

- Выучить основы bash и python/go (дополнительная информация ниже в `Базовые знания Linux, сетей и bash скриптов`)
- Из операционных систем советую поставить себе Ubuntu: https://ubuntu.com/desktop
   > Большинство серверов работают на linux и Ubuntu будет удобен в обычном пользовании и подготовке к работе
- Из текстовых редакторов научиться открывать файлы и редактировать в `nano`, а также в `vim` (если удобно)
- По терминалу вся информация будет в `Базовые знания Linux, сетей и bash скриптов`
- По системе контроля версий git ниже в `Git система контроля версий и автоматизация с помощью GitLab CI/CD`
- По контейнеризации изучать Docker, ниже в `Контейнеризация с помощью Docker и Kubernetes`
- Насчет Облачных провайдеров, в России лучше использовать Yandex Cloud, SberCloud или VK Cloud
- Сети изучать ниже в `Базовые знания Linux, сетей и bash скриптов`
- Изучать Terraform и Ansible как IaC (инфраструктуру как код, ниже в `IaC - (Инфраструктура как код) создание серверов с помощью Terraform и настройка с помощью Ansible`)
- CI/CD проще изучать на основе GitHub Actions, а потом GitLab CI/CD (автоматизация)
- 

Полезные youtube каналы:
- Канал с плейлистами по которому учились многие devops инженеры: https://www.youtube.com/@ADV-IT/playlists
- Канал планых курсов Merion Academy на котором рассказывают про технологии из RoadMap выше простыми словами: https://www.youtube.com/watch?v=NtGN7Nz6I0c
- Хороший канал по devops, все видео смотреть на скорости 1.25 (если не хотите заснуть): https://www.youtube.com/@pavlenkoat/playlists

Ниже используем видео с этих каналов для ознаколмения с тенологиями:

<details>
  <summary>Базовые знания Linux, сетей и bash скриптов</summary>

| Цель и что нужно для изучения + Задания | Как поймем что цель достигнута? |
|-|-
| Linux - ядро операционной системы, например Ubuntu построена на базе Linux. Пройти курс https://youtu.be/wdaHKwvNRuU?si=UnvTogPjiVOE5PEc и сделать все задания https://github.com/eabykov/devops-linux | Может устанавливать программы, знает основные команды и может их применять, что такое ядро linux, знает какие основные папки есть в `/`, отвечает на вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/linux и https://github.com/bregman-arie/devops-exercises#operating-system---self-assessment
| Linux скрипты - простые сценарии, автоматизация рутинных задач. Задание: сделать скрипты для всех заданий https://github.com/eabykov/devops-linux и задания 2,5,9 в https://github.com/bregman-arie/devops-exercises/tree/master/topics/shell | Умеет создавать и использовать переменные, может применять условный оператор IF и использовать CASE, умеет использовать циклы, вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/shell
| Сети и сетевые технологии - как сервера (настольные ПК и тд) обьеденятются в общую сеть для обмена информацией, пример интернет, глобальная сеть обьеденяющая компьютеры по всему миру. Прочесть статью https://habr.com/ru/post/326574/ , https://ru.wikipedia.org/wiki/Маска_подсети и https://habr.com/ru/post/711578/ , посмотреть про websocket https://youtu.be/19d4AXt3dSI | Как подключиться по SSH и как роаботает SSH, что такое 'пакет', уровни TCP/IP, что такое DNS, что такое HTTP/HTTPS протокол и REST API, что такое IP и маска подсети, как на linux посмотреть сетевые интерфейсы, сниффинг трафика, что такое Nginx (как выглядит конфиг) и round-robin балансировка, вопросы https://github.com/bregman-arie/devops-exercises#network и https://github.com/bregman-arie/devops-exercises/tree/master/topics/dns

</details>

<details>
  <summary>Git система контроля версий и автоматизация с помощью GitLab CI/CD</summary>

| Цель и что нужно для изучения + Задания | Как поймем что цель достигнута?
|-|-|
| Git - система управления версиями для совместной работы над проектом и в случае чего удобному восстановлению к более старой версии https://youtu.be/EeARyFrZsnU . Пройти курс https://www.youtube.com/watch?list=PLg5SS_4L6LYstwxTEOU05E0URTHnbtA0l до 15 урока и создать свой репозиторий на github с несколькими ветками и тегами | Знает что такое commit и как его делать, умеет делать branch и tag и знает в чем между ними разница, знает что такое merge и как исправлять конфликты, знает как откатиться на более старую версию, как склонировать репозиторий локально и как загрузить свои изменения в github, в чем разница межу fetch и pull, вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/git
| CI/CD - выполнение автоматически действий по триггеру, например commit в master, создание merge, создание tag или cron расписанию. В курсе https://www.youtube.com/watch?list=PLg5SS_4L6LYstwxTEOU05E0URTHnbtA0l 15й и 16й, https://youtu.be/tE3u1LquFcg?t=212 скорость 1.25, https://github.com/gitlabhq/gitlabhq/blob/master/doc/ci/docker/using_kaniko.md `.gitlab-ci.yml` как собирать Docker Image в GitLab правильно | Сделал автоматическую сборку своего Docker Image и отправку dockerhub хранилище образов (хранилище образов называют registry), GitLab CI/CD основные понятия, из каких шагов состоит идеальный CI/CD пайплайн, вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/cicd

</details>

<details>
  <summary>Контейнеризация с помощью Docker и Kubernetes</summary>

| Цель и что нужно для изучения + Задания | Как поймем что цель достигнута?
|-|-|
| Docker - упаковка приложения в image в котором будет все что нужно для запуска https://youtu.be/aZTL2zRmOnA | Понимает зачем нужен docker, умеет создавать свой образ и пушить его в dockerhub, умеет запускать несколько образов вместе используя compose, вопросы https://habr.com/ru/company/southbridge/blog/528206/
| Kubernetes - приводит состояние кластера из пункта А в пункт С, нужно только обьяснить с помощью yaml манифестов чего хотим в пункте С. Пройти курс https://learn.microsoft.com/ru-ru/training/modules/intro-to-kubernetes/ вместе с https://github.com/eabykov/kubernetes и поставить локально linkerd (посмотреть какие сервисы взаимодействуют, есть ли ошибки, сколько запросов в секунду) | Понимает зачем нужен Kubernetes, как устанавливать приложения через helm, вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/kubernetes

Примерный порядок изучения технологии:
- Docker: https://roadmap.sh/docker
- Kubernetes: https://roadmap.sh/kubernetes

</details>

<details>
  <summary>Мониторинг, золотые сигналы и логгирование</summary>

| Цель и что нужно для изучения + Задания | Как поймем что цель достигнута?
|-|-|
| Мониторинг - сбор исторических данных о нашей системе https://youtu.be/wDan20_WyNg использовать пример https://github.com/ruanbekker/docker-monitoring-stack-gpnc , Linux серверах, показателей приложений и их логов, сетевых метрик, оповещение если что-то пошло не так. Prometheus + Grafana + любые экспортеры, ELK стек https://youtu.be/ZcC3BTChCY0?t=110 и https://github.com/docker/awesome-compose/tree/master/elasticsearch-logstash-kibana , Трейсинг https://youtu.be/7Dyf4AiUAcQ | Понимает как создавать алерты (оповещения), может настроить мониторинг Docker, linux host, в Kubernetes установить https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack , вопросы https://github.com/bregman-arie/devops-exercises#prometheus , https://github.com/bregman-arie/devops-exercises#monitoring и https://github.com/bregman-arie/devops-exercises#elastic

Логгирование в Kubernetes: https://kubernetes.io/docs/concepts/cluster-administration/logging/

Золотые сигналы: https://habr.com/ru/companies/southbridge/articles/688082/
- Процент успешных запросов
- RPS (requests per second) - количество запросов в секунду
- время обработки запросов

Автоматический мониторинг золотых сигналов (Golden metrics) с помощью Linkerd: https://linkerd.io/2.13/features/telemetry/

Пример алерта в AlertManager который срабатывает по условию из Prometheus

```yaml
- name: Host out of memory
  # description - описание алерта, более детальное пояснение о чем он
  description: Node memory is filling up (< 10% left)
  # query - запрос в случае которого будет срабатывать алерт, правило (например памяти меньше 10%)
  query: '(node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes * 100 < 10) * on(instance) group_left (nodename) node_uname_info{nodename=~".+"}'
  # severity - уровень алертинга, важность, например warning это предупреждение, а critical критично и опасно - самый большой приоритет
  severity: warning
  # for - сколько минут должно соблюдаться 'query' выше, 0m сработает алерт сразу, 2m правило в query должно соблюдаться 2 минуты
  for: 2m
```
> Готовые алерты брать тут: https://github.com/samber/awesome-prometheus-alerts/blob/master/_data/rules.yml

Примеры работы с логами в ELK: 
- Приложения database записывает логи на диск в файл: `2023-10-11 18:45:01 INFO Application ready`
- Приложения web-app записывает логи на диск в файл: `18:45:02 2023-10-11 error: failed to start`

Логи которые попадут в Elasticsearch (формат `JSON`):
```json
{"program_name": "database", "date": "2023-10-11", "time": "18:45:01", "level": "INFO", "message": "Application ready"}
{"program_name": "web-app", "date": "2023-10-11", "time": "18:45:02", "level": "ERROR", "message": "failed to start"}
```

</details>

<details>
  <summary>IaC - (Инфраструктура как код) создание серверов с помощью Terraform и настройка с помощью Ansible</summary>

| Цель и что нужно для изучения + Задания | Как поймем что цель достигнута?
|-|-|
| Ansible - упарвляет конфигурацией хостов по SSH https://youtu.be/23Zec3ORJOY . Пройти курс https://www.youtube.com/watch?list=PLg5SS_4L6LYufspdPupdynbMQTBnZd31N 1,6,10,12,14,15,19 не по названию | Понимает зачем нужен Ansible, что такое идемпотентность, что такое playbook, умеет писать свои роли, вопросы https://github.com/bregman-arie/devops-exercises/tree/master/topics/ansible
| Terraform https://youtu.be/ph4iNA0Uuko . Пройти курс https://www.youtube.com/watch?list=PLg5SS_4L6LYujWDTYb-Zbofdl44Jxb2l8 1,3,6,7,12,14,16,18 не по названию | Понимает зачем нужен Terraform, знает как создавать ресурсы (например виртуальную машину), где хранится состояние (информация) о том что сделал terraform, вопросы https://habr.com/ru/company/southbridge/blog/528206/

Генерация пары SSH ключей:
```sh
ssh-keygen -t ed25519 -C 'ВАШ АДРЕС ЭЛЕКТРОННОЙ ПОЧТЫ'
```

Файловая структура Ansible role:
```
roles/                      # роли хранятся в папке 'roles'
    prometheus/             # имя роли, в нашем случае 'prometheus'
        tasks/
            main.yml        #  ниже пример файла
        files/
            prometheus.conf #  файл который будет скопирован на удаленную машину
        vars/
            main.yml        #  переменные для данной роли, например версия prometheus
        defaults/
            main.yml        #  самые базовые переменные по умолчанию, имеют ниже приоритет чем 'vars' выше
```

Пример файла `roles/prometheus/tasks/main.yml`:

```yaml
- name: Install prometheus # устанавливаем prometheus на удаленном сервере
  ansible.builtin.apt:
    name: prometheus       # какую программу будет устанавливать

- name: Copy prometheus config to remote hosts # имя задачи, чтобы мы понимали что делает
  ansible.builtin.copy:
    src: prometheus.conf                  # где файл лежит у нас на компе
    dest: /etc/prometheus/prometheus.conf # то куда файл попадет на удаленных хостах
    owner: aider                          # кто будет хозяином файла на удаленной машине
    group: aider                          # какая группа будет у файла на удаленной машине
    mode: u=rw,g=r,o=r                    # какие права будут у файла на удаленной машине

- name: restart prometheus # перезапустить prometheus
  service:
    name: prometheus  # с каким сервисом будем работать
    state: restarted  # перезапустить prometheus
    enabled: yes      # запускать nginx при перезапуске системы
```

</details>

Вопросы на собеседованиях: [ВОПРОСЫ_НА_СОБЕСЕДОВАНИИ.md](ВОПРОСЫ_НА_СОБЕСЕДОВАНИИ.md)
