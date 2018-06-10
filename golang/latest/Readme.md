## About
- Based on docker image golang 

## How to use?
### 为了避免宿主机没有装golang环境,ide无法自动提示,目前自己想到比较糙的办法是:
1.将容器中gorootd复制一份到宿主机,在宿主机命令行执行:
``` go
docker cp container-name:/usr/local/go $HOME/code/goroot
```
  -  上述中container-name是容器的名词或在id,后根容器中goroot的路径.不同安装可能不一样.进入容器go env查看
  -  最后跟要复制到宿主机的路径

2.将宿主机中从容器中复制出来的goroot重新挂载到容器:
``` go
docker run --name golang -p 8088:8088 -v $HOME/code/goroot:/usr/local/go -v $HOME/code/go:/go --privileged=true -it yin5th/golang /bin/bash
```
3.针对步骤2的解释.重新挂载到容器,是为了确保容器中可能出现的go get等情况下,宿主机能保持一致
