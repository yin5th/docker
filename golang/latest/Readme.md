## About
- Based on docker image golang 

## How to use?
### 为了避免宿主机没有装golang环境,ide无法自动提示,目前自己想到比较糙的办法是:
1. 将容器中gorootd复制一份到宿主机,在宿主机命令行执行:
`` 
  docker cp container-name:/usr/local/go $HOME/code/goroot
``
2. 将宿主机中从容器中复制出来的goroot重新挂载到容器:

`` 

  docker run --name golang -p 8088:8088 -v $HOME/code/goroot:/usr/local/go -v $HOME/code/go:/go --privileged=true -it yin5th/golang /bin/bash

``
3. 针对步骤2的解释.重新挂载到容器,是为了确保容器中可能出现的go get等情况下,宿主机能保持一致 
