#how to use this docker-compose
  
   #start container
   docker-compose up
   
   #Stop and remove containers, networks, images, and volumes
   docker-compose down

   #delete container
   docker rm $(docker ps -a|grep jason|awk '{print $1}' )
	
	#delete images
	docker rmi $(docker images|egrep "mysql-redis-web-nginx"|awk '{print $1}' )
Notes:

   mysql:  my.cnf 如下配置   
   [mysqld]
   character-set-server = utf8mb4
   collation-server = utf8mb4_unicode_ci
   performance_schema = OFF
   

   
