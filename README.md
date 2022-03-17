# Docker-Hexo
> by Cyris Tseng

## Note
- Based on [node:12.22-bullseye](https://hub.docker.com/_/node)
    - This image variant include additional related tools (such as git or bash).
    - Because of `nib/stylus` incompatible, see [issue](https://github.com/nodejs/node/issues/32987)
- default user: root:hexo
    - **You must change your password using `passwd` command**

### Usage
```
$ docker-compose up --build -d
$ docker exec -it [container_id] bash
(docker)$ passwd # change password
```
