# MySQL 5.6
--

###Start the MySQL Server
```
    docker run \ 
    -idt \
    -p 3306:3306 \
    -v <data_path>:/var/lib/mysql \
    --name mysql \
    -e MYSQL_ROOT_PASSWORD=root \
    berialcheng/docker-mysql
```

###Connect through shell
```
	docker run \
	-it \
	--link mysql:mysql \
	--rm \
	-v /Users:/tmp \
	mysql:5.6 bash

	mysql -hmysql -uroot -proot
```