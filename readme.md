## 使用

1. 新建/usr/local/docker-apps/文件夹：存放运行的项目。

   ```bash
   mkdir -p /usr/local/docker-apps/
   ```
   
2. 拉取videoDocker项目并修改项目名：

   ```bash
   git clone https://github.com/zqyp/videoDocker.git
   mv /videoDocker video
   ```

3. 进入video/app/下，放入项目启动需要的video-0.0.1-SNAPSHOT.jar、application.yml、camera.txt文件。

4. 两种启动方式：

   1） 拉取制作好的镜像，步骤简单。

      与docker-compose-hub.ym同层目录，运行docker-compose-hub.yml,启动项目：

      ```bash
      docker-compose -f docker-compose-hub.yml up -d
      ```

   2） 重新build镜像。 

      （1） 在docker-apps/文件夹下，拉取nginx-http-flv:

      ```bash
      git clone https://github.com/zqyp/nginx-http-flv.git
      ```

      （2）与docker-compose-build.ym同层目， 运行docker-compose-build.yml（build）,启动项目：

      ```bash
      docker-compose -f docker-compose-build.yml up -d
      ```

      