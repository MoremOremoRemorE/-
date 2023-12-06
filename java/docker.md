## docker面试问题
1. 你们都是怎么使用docker的
    > 使用docker部署项目，生成docker镜像给客户
2. 部署在docker中的程序外部不能访问，应该怎么排查
    > 首先判断是否是网络的问题，使用docker inspect 查看当前docker容器的ip地址，使用docker port 查看容器使用的端口，在外部使用ping或者telnet等命令查看网络是否通
    > 网络问题排查完后，使用docker logs命令查看容器的日志，查看是否服务报错
3. docker怎么部署springboot项目
    > 1. 写好dockerFile文件，使用docker build命令将项目的jar打成docker镜像
    > 2. 使用docker save -o 将镜像打成tar压缩包
    > 3. 使用docker load -i 命令将tar解压成docker image
    > 4. 使用docker run 或者docker-compose命令启动docker镜像

