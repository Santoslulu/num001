
<h1 align="center"> 免责声明 </h1>


<p align="center">
仅供科研学习之用，切勿用于其他用途，否则出现一切问题，项目作者概不负责
</p>
<hr>



# v2ray 部署在 openshift starter

1、fork 本项目到自己的Github；

2、建立docker镜像：

A、https://hub.docker.com/

B、connect to Github:
    "sign in" - "Account Settings" -"Linked Accounts"
  C、Repositories
    "Create Repository"
3、Project
  A、https://www.openshift.com/
  B、add project:
    "add project" - "deploy image" - 选择2建立的镜像 - deploy it
  C、
    
鉴于转载网友太多，甚至还发到了国内网站上宣传，为避免不必要麻烦，docker镜像已经删除，需要的请自行fork本
项目，然后照着这个视频 https://youtu.be/gImm4CfAnRs 自行部署镜像！ 2018/09/26

（fork于wangyi2005/v2ray修改前）

环境变量： CONFIG_JSON（配置）、


用notepad++将上述变量中 \r\n 替换为\\n，变成一行，导入容器。

客户端： android Actinium、windows v2ray 可用同一个服务端。

youtube频道：https://www.youtube.com/channel/UClceV39J1Z_9D4_mHkBZrMg

