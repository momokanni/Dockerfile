命令：  

`docker run -d --memory 300M --hostname rabbit --name rabbit_service -p 5672:5672 -p 15672:15672 --network cloud_bridge rabbitmq:3.7.8-management
`  
`docker exec -it rabbit_service /bin/bash`  

`rabbitmqctl add_user 用户名 密码`  

`rabbitmqctl set_user_tags 用户名 角色(administrator)`  

`rabbitmqctl set_permissions -p "/" admin ".*" ".*" ".*"`  
