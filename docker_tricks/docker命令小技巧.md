docker images -f since=mysql:5.7  mysql:5.7之后下载的所有镜像  
docker images -f before=mysql:5.7  mysql：5.7之前下载的所有镜像  
docker images "mys*:*"            匹配mys*：*的所有镜像  
docker images -f "dangling=true"//未贴标签的  

配合rmi可以比较随心所欲的删除镜像  
docker rmi $(docker images -f since=mysql:5.7 -q)  
