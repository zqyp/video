### 说明
   这是一个使用docker 启动app/ 下指定xxx.jar的项目，参见deploy/下的dockerfile文件配置。

---

### 使用
   
1. 在任意路径下（path1），拉取video项目：

   ```shell
   git clone https://github.com/zqyp/video.git
   ```
   
   或
   
   ```shell
    git clone git://github.com/zqyp/video.git
    ```
    

3. 进入app/下，放入项目启动需要的video-0.0.1-SNAPSHOT.jar、application.yml、camera.txt文件。

4. 两种启动方式：

   1） 拉取制作好的镜像，步骤简单。

      进入video/，运行docker-compose-hub.yml,启动项目：

      ```bash
      docker-compose -f docker-compose-hub.yml up -d
      ```

   2） 重新build镜像。 

      （1） 在path1下，拉取nginx-http-flv:

      ```shell
      git clone https://github.com/zqyp/nginx-http-flv.git
      ```

      （2）进入video/， 运行docker-compose-build.yml（build）,启动项目：

      ```shell
      docker-compose -f docker-compose-build.yml up -d
      ```

      
