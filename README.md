# docker-php
docker的 nginx + php + mysql集成环境

如何启动?

1. 拉去代码到本地
2. 创建代码目录  不改配置的前提下,代码需要放在 docker-php目录/code/server, 或者随意放置代码位置, 修改docker-compose.yaml文件,有两处 $PWD/code/server改为自己的代码路径
3. 再docker-php目录 下执行命令  docker compose up -d
