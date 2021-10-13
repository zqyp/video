## app是存放挂载信息的文件夹，存放springboot.jar和外部可修改的文件。
## deploy是docker创建镜像的文件夹。

1. 进入deploy, build

   ```bash
   docker build -t zzpp/video:v2 .
   ```

2. run

   ```bash
   docker run -d -p 8003:8003 --name video -e TZ="Asia/Shanghai" -v /etc/localtime:/etc/localtime:ro -v /usr/local/docker-apps/video/app:/usr/local/docker-apps/video/app zzpp/video:v2
   ```

   

#### 挂载主机时间 统一时区
-e TZ="Asia/Shanghai" -v /etc/localtime:/etc/localtime:ro 
