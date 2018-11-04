#### spring-cloud-config Dockerfile 示例

config依赖于Eureka、rabbitMQ，所以就会涉及到 **容器间请求**。  
>1. 创建Driver为bridge的网络。并将三个服务connect该网络。  
>2. 进入到各个容器中，通过`ping 容器名` 测试网络连接状态  
>3. 将应用程序配置文件中的所有服务路径涉及到的IP改为container_name  


## 大坑槽（死坑）  
新建user和guest的账户是没有远程登录的权限的 需要对登录账户授权  
创建用户： `rabbitmqctl add_user 用户名 密码`  
设定角色： `rabbitmqctl set_user_tags 用户名 角色(administrator)`  
赋权： `rabbitmqctl set_permissions -p "/" admin ".*" ".*" ".*" `
