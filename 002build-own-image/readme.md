1. [docker hub](https://hub.docker.com/) 中查找image(repo)
    
2. 使用 docker/whalesay image创建docker container

    `docker run docker/whalesay cowsay heiliuer`
    
    > container 启动后运行命令 cowsay heiliuer cowsay是container一个小游戏程序
        
3. 创建自己的image
    
    - 新建编辑 `mydockerbuild/Dockerfile` 文件，
    
    - 在 `mydockerbuild` 目录下执行命令
    
        `docker build -t docker-whale .` 读取当前目录的Dockerfile配置，创建名为 docker-whale 的docker image
        
        `docker run docker-whale .` 运行创建的 image

4. 关联image 到 docker hub 的 repo

    `docker tag <image id> heiliuer/docker-whale:latest`
    
    `docker login`
    
    `docker push heiliuer/docker-whale`
    
5. pull image
    
    - remove image
        
        `docker rmi -f <image name> or <image name>`
        
    - pull and run image
    
        `docker pull  heiliuer/docker-whale`
        
        or
        
        `docker run heiliuer/docker-whale`
        
6. 后台一直运行ubuntu

    `docker run --name ubuntu -d ubuntu /bin/sh -c "while true; do ping 8.8.8.8; done"`
    
    `docker log ubuntu` 查看container 日志docker 命令 的输出
    
    `docker exec -it ubuntu /bin/bash` 执行ubuntu的shell，进行shell交互