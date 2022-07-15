# isolated-docker-playground

## supported-container

you can run container partially using `docker compose up $name`

- [ ] airflow (for local dev, not production)

  - https://airflow.apache.org/docs/apache-airflow/stable/start/docker.html#
  - Default amount of memory available for Docker on MacOS is often not enough to get Airflow up and running. If enough memory is not allocated, it might lead to airflow webserver continuously restarting. You should at least allocate 4GB memory for the Docker Engine (ideally 8GB)
  - https://wooiljeong.github.io/server/docker-airflow/
    - if you get some trouble, just drop container `docker-compose down --volumes --remove-orphans`

- [ ] mysql

  - https://hub.docker.com/_/mysql
  - ```
    docker exec -it CONTAINER_ID /bin/bash # mysql 컨테이너 내부 접속
    mysql -u root -p # 접속
    ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password by 'yourpassword';
    FLUSH PRIVILEGES;
    ```

- [ ] postgresql

  - https://hub.docker.com/_/postgres
  - ```
    psql -U $name
    ```

- [ ] nginx
  - https://hub.docker.com/_/nginx
  - official doc: http://nginx.org/en/docs/
  - ```
    docker compose up
    ```

## materials

https://docs.docker.com/engine/reference/commandline/compose/

## etc

docker-compose config
