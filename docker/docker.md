DOCKER
=======
安装
-------
#TODO

简介
------
#TODO

使用
------
### 镜像的使用
* docker images
<p>查看本地镜像</p>

* docker search mysql:'version'
<p>搜寻仓库镜像</p>

* dcoker pull mysql
<p>从仓库拉取仓库镜像</p>

* docker run -itd --name mysql-test -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password mysql
<p>运行镜像，创建容器</p>

* * 参数说明
* * `-p 3306:3306` 映射容器服务的 `3306` 端口到宿主机的 `3306` 端口，外部主机可以直接通过 宿主机`ip:3306` 访问到 `MySQL` 的服务
* * `MYSQL_ROOT_PASSWORD=123456` 设置 `MySQL` 服务 `root` 用户的密码
* * `-v /opt/docker_v/mysql/conf:/etc/mysql/conf.d` 将主机 `/opt/docker_v/mysql/conf` 目录挂载到容器的 `/etc/mysql/conf.d`
* * `-i` 交互式操作
* * `-t` 终端
* * `-d` 后台运行容器，并返回容器ID

* docker rmi mysql
<p>删除镜像</p>

* 更新镜像
<p>#TODO</p>

* 创建镜像
<p>#TODO</p>

### 容器的使用
* docker ps -a
<p>查看容器</p>

* docker stop/restart <容器 ID>
<p>停止/重启容器</p>

* docker exec -it 243c32535da7 /bin/bash
<p>进入</p>

* docker export 1e560fca3906 > ubuntu.tar
<p>导出容器</p>

* cat docker/ubuntu.tar | docker import - test/ubuntu:v1
* docker import http://example.com/exampleimage.tgz example/imagerepo
- 导入容器的两种方式： 1.使用 `docker import` 从容器快照文件中再导入为镜像，以下实例将快照文件 `ubuntu.tar` 导入到镜像 `test/ubuntu:v1`. 2.通过指定 `URL` 或者某个`目录`来导入</p>

* docker rm -f 1e560fca3906
<p>删除容器</p>

[docker 教程(runoob.com)](https://www.runoob.com/docker/docker-tutorial.html)
