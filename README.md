# Laravel-приложение в docker-контейнерах
Этот проект представляет собой контейнеризированное приложение Laravel, готовое к использованию с помощью Docker. (автор)

## **Структура проекта**

```bash
laravel-app-dockerized/
├── dockerfiles/
│   ├── composer.Dockerfile
│   └── php.Dockerfile
├── env/
│   └── postgres.env
├── nginx/
│   └── nginx.conf
└── docker-compose.yaml
```

- **dockerfiles/**: Директория, содержащая Docker-файлы для компонента Composer и PHP.
- **env/**: Директория, где находится файл с переменными окружения для PostgreSQL.
- **nginx/**: Директория с конфигурационным файлом Nginx.
- **docker-compose.yaml**: Файл, определяющий структуру и настройки Docker-контейнеров.

## **Запуск приложения**

1. Убедитесь, что у вас установлен Docker и Docker Compose.
2. Клонируйте репозиторий на локальную машину:
    
    ```bash
    git clone git@github.com:jibunnoeiko/Laravel-app-in-docker.git
    ```
    
3. Перейдите в директорию проекта:
    
    ```bash
    cd laravel-app-dockerized
    ```
5. Запустите приложение с помощью Docker Compose:
    
    ```css
    docker-compose up nginx -d --build
    ```
    
6. После успешного запуска, приложение будет доступно по адресу http://localhost/8000.

## **Дополнительные настройки**

- **Настройка Базы Данных**: Если требуется изменить настройки базы данных PostgreSQL, отредактируйте файл **`postgres.env`** в директории **`env/`**.
- **Настройка Nginx**: При необходимости измените конфигурацию в файле **`nginx.conf`** в директории **`nginx/`**.
- **Другие настройки**: Дополнительные настройки Docker и Laravel можно произвести в соответствующих файлах Docker-композиции и конфигурационных файлах Laravel.

## **Остановка приложения**

Для остановки приложения выполните следующую команду:

```
docker-compose down
```

Это остановит и удалит контейнеры, созданные для приложения.

## **Важно**

- Перед запуском убедитесь, что порты, используемые приложением, не заняты другими процессами.
- Не забудьте выполнить миграции и настройку Laravel после запуска контейнеров, если это необходимо.
- Не забываем установить зависимости 

---
