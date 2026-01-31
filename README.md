# Урок. Контейнеризация. Знакомство с Docker

## Задание

### 1. Запустить интерактивно образ ubuntu и открыть консоль bash внутри контейнера

**Команда:**
```bash
docker run -i -t ubuntu /bin/bash
```

**Скриншот выполнения:**  
![Задание 1](https://github.com/ваш-username/ваш-репозиторий/blob/main/screenshots/1.png)  
*Запуск интерактивного контейнера Ubuntu*

---

### 2. Запустить контейнер docker/getting-started в фоновом режиме с маппингом портов 80:80

**Команда:**
```bash
docker run -d -p 80:80 docker/getting-started
```

**Скриншот выполнения:**  
![Задание 2](https://github.com/ваш-username/ваш-репозиторий/blob/main/screenshots/2.png)  
*Запуск контейнера getting-started в фоновом режиме*

---

### 3. Найти контейнер в системе командой docker ps и узнать id. Использовав id, остановить контейнер

**Команды:**
```bash
docker ps
docker stop <container_id>
```

**Скриншот выполнения:**  
![Задание 3](https://github.com/ваш-username/ваш-репозиторий/blob/main/screenshots/3.png)  
*Поиск и остановка контейнера*

---

### 4. Запустить локальный registry и запушить в него образ

**Команды:**
```bash
docker run -d -p 5000:5000 --name registry registry:2
docker tag hello-world localhost:5000/my-hello-world
docker push localhost:5000/my-hello-world
curl http://localhost:5000/v2/_catalog
```

**Скриншот выполнения:**  
![Задание 4](https://github.com/ваш-username/ваш-репозиторий/blob/main/screenshots/4.png)  
*Работа с локальным registry*

---

## Выводы

В ходе выполнения задания были освоены базовые операции работы с Docker:
1. Запуск контейнеров в интерактивном и фоновом режимах
2. Маппинг портов между хостом и контейнером
3. Управление жизненным циклом контейнеров (запуск, просмотр, остановка)
4. Работа с образами Docker (тегирование, работа с локальным registry)

