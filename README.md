
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
      
      将"confit.json"文件用notepad++打开，将全文的 \r\n 替换为\n，（记得选择循环查找和正则表达式方式)，复制
      
      在"容器"中,粘贴，变成一行
      
      在下面点击"添加"
      
      点击"部署"
      
    D、创建完成后，在新页面点击"Create router"
      
      点击"Secure router"
        
      选择"TLS Termination"下的第一选项"Edge"
        
      到最下面，点击"创建"
        
    E、完成后，出现网址链接"https://AAAA.BBBB.starter-us-west-2.openshiftapps.com"
      
      打开链接，显示"Bad Request"
        
4、v2ray客户端设置

    添加服务器
    
        "地址"，将不含"https://" 的"AAAA.BBBB.starter-us-west-2.openshiftapps.com"填入
        
        "端口" - 443
        
        "用户ID" - config.json中的ID
        
        "额外ID" - 64
        
        "加密方式" - config.json中的加密方式(如"aes-128-gcm")
        
        "传输协议" - ws
        
        "底层传输安全" - tls
        
注：docker部署视频 https://youtu.be/gImm4CfAnRs

   openshift部署视频：https://www.youtube.com/watch?v=s83EXZbb8vQ

   环境变量： CONFIG_JSON（配置）、

   客户端： android Actinium、windows v2ray 可用同一个服务端。
