1. docker build -t zzpp/video:v2 .
2. docker run -d -p 8003:8003 --name video -e TZ="Asia/Shanghai" -v /etc/localtime:/etc/localtime:ro -v /usr/local/docker-apps/video/app:/usr/local/docker-apps/video/app zzpp/video:v2
3. docker exec -it video /bin/bash

## 挂载主机时间 统一时区
-e TZ="Asia/Shanghai" -v /etc/localtime:/etc/localtime:ro 
