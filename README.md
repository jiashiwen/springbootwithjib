# springbootwithjib

## 目的
* 该工程用于验证google 镜像工具jib与springboot集成
* pom.xml中的提交仓库为私有仓库，需要自建，自建方式[参考文档](https://www.jdcloud.com/help/detail/3050/isCatalog/1)
* mvn compile jib:build 命令可正常构建镜像并推送至镜像仓库

## 坑
* 虽然镜像推送成功并可以正常下载运行，但harbor web页面不能正常显示，原因是由于jib中使用了自定义User-Agent value。目前社区无法解决。如果想让镜像在web中显示目前只能用docker客户端从新推送一遍

## 待解决问题
