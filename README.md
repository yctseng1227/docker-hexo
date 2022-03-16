# Hexo Docker

## Note
- Based on [node:16.14-bullseye]()
- default user: root:hexo
    - **You must change your password using `passwd` command**

### Usage
```
$ docker-compose up --build -d
$ docker exec -it [container_id] bash
(docker)$ passwd # change password
```
