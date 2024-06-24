![image](https://github.com/henkel-v/Laravel-app-in-docker/assets/62598594/b35b3b84-a5fc-48c4-84ff-9b10ac08ece3)
# Laravel application in docker containers
This project is a containerised Laravel application ready to use with Docker. 

## **Project structure**

```bash
laravel-app-dockerized/
├── docker/
│   ├── dockerfiles/
│   │   ├── composer.Dockerfile
│   │   └── php.Dockerfile
│   └── php/
│       └── conf.d/
│           ├── error_reporting.ini
│           └── xdebug.ini
├── env/
│   └── postgres.env
├── nginx/
│   └── nginx.conf
└── docker-compose.yaml
```

- **dockerfiles/**: The directory containing the Docker files for the Composer component and PHP.
- **env/**: The directory where the file with environment variables for PostgreSQL is located.
- **nginx/**: The directory with the Nginx configuration file.
- **docker-compose.yaml**: A file that defines the structure and settings of Docker containers.

## **Launching an application**

1. Make sure you have Docker and Docker Compose installed.
2. Clone the repository to your local machine:
    
    ```bash
    git clone git@github.com:jibunnoeiko/Laravel-app-in-docker.git
    ```
    
3. Navigate to the project directory:
    
    ```bash
    cd laravel-app-dockerized
    ```
5. Build the application using Docker Compose:
    
    ```css
    docker-compose up nginx -d --build
    ```
    
6. After successful launch, the application will be available at http://localhost/8000


## **Additional Settings**

- **Database Settings**: If you want to change the PostgreSQL database settings, edit the **`postgres.env`** file in the **`env/`** directory.
- **Nginx Configuration**: If necessary, change the configuration in the **`nginx.conf`** file in the **`nginx/`** directory.
- **Other Settings**: Additional Docker and Laravel customisations can be made in the respective Docker composition files and Laravel configuration files.

## **Stop Application**

To stop the application, run the following command:

```
docker-compose down
```

This will stop and delete the containers created for the application.

## **Important**

- Before launching, make sure that the ports used by the application are not occupied by other processes.
- Don't forget to perform Laravel migrations and configuration after running the containers, if necessary.
- Don't forget to install dependencies 

---
