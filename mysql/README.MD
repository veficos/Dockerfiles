
## build 

docker build . -t alpine-mysql

## run 

docker run -it --name mysql -p 3306:3306 -v $(pwd):/app -e MYSQL_DATABASE=admin -e MYSQL_USER={YOURUSERNAME} -e MYSQL_PASSWORD={YOURPASSWORD} -e MYSQL_ROOT_PASSWORD=111111 alpine-mysql
