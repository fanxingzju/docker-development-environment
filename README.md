## 构建镜像

以clion镜像为例，可以使用如下命令构建镜像

```bash
cd docker_develop_images/clion_20190104
docker build -t clion:20190104 ./
```

备注： 如果需要使用代理，可以参考如下的命令(需要换成自己的proxy地址和端口号)

```bash
cd docker_develop_images/clion_20190104
docker build --network host \
    --build-arg HTTPS_PROXY=https://127.0.0.1:1080 \
    --build-arg HTTP_PROXY=http://127.0.0.1:1080 \
    -t clion:20190104 ./
```

参考：[docker build命令](https://docs.docker.com/engine/reference/commandline/build/)

## 启动容器

参考[容器化开发环境](https://github.com/fanxingzju/docker_development_images/blob/master/docs/容器化开发环境.md)

注意配置x11-server及设置DISPLAY环境变量

## 进入容器

```bash
docker exec -it container_name /bin/bash
```

其中，container_name是启动容器时指定的容器名字。
