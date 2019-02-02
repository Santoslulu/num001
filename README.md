
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
      
      B、project:
      
        登陆openshift点击进入控制台 - "Create Project"
        
        点击创建完成的项目，进入新页面；
        
        点击deploy image按钮，选择image name，输入2中创建的docker镜像名，AAAAA/BBBBB，点击搜索按钮
        
        搜索到后，
                
      C、搜索到后,在"环境变量"中输入"CONFIG_JSON"
      
      将"confit.json"文件用notepad++打开，将全文的 \r\n 替换为\\n，复制
      
      在"容器"中,粘贴，变成一行
      
      在下面点击"添加"
      
      点击"部署"
      
      选择"ws"
    
鉴于转载网友太多，甚至还发到了国内网站上宣传，为避免不必要麻烦，docker镜像已经删除，需要的请自行fork本
项目，然后照着这个视频 https://youtu.be/gImm4CfAnRs 自行部署镜像！ 2018/09/26

（fork于wangyi2005/v2ray修改前）

环境变量： CONFIG_JSON（配置）、


用notepad++将上述变量中 \r\n 替换为\\n，变成一行，导入容器。

客户端： android Actinium、windows v2ray 可用同一个服务端。

youtube频道：https://www.youtube.com/channel/UClceV39J1Z_9D4_mHkBZrMg

