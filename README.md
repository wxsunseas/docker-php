# docker-php

docker的 nginx + php + mysql集成环境

如何启动?

1. 拉去代码到本地
2. 创建代码目录  不改配置的前提下,代码需要放在 docker-php目录/code/server, 或者随意放置代码位置, 修改.env文件 APPDIR的值
3. 在docker-php目录 下执行命令  docker compose up -d

注:

1. 默认mysql 和 php 端口不开放使用
2. 如果需要开放出来使用, 第三步命令改为 ``docker compose -f docker-compose.yaml -f docker-compose.dev.yaml up -d``
3. php 添加插件库
   1. [Dockerfile](./env/php/Dockerfile)中添加所需要的库
   2. php.ini 中也需要将相应的注释去掉
