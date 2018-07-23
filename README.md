# dockerfiles notes

新建镜像 进入dockerfile文件所在目录
docker build -t ai_ocr:20180315 .

 暂停 dockerfile下载出错的docker
docker ps -a|awk '{print $1}'|xargs docker rm

运行docker 挂载文件到docker 需要指定source 和 target 
nvidia-docker run -it -P --mount type=bind,source=$HOME/文档/image_demo,target=/usr/demo ai_images:20180314 
