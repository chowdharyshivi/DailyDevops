
# Task CheckList 
1. Lookup phpMyAdmin image on DockerHub
2. Pull phpMyAdmin image
3. Run the phpMyAdmin image with intended flags
4. Access the admin page in your browser  


1.   Pull MySQL image and run inside container.
    - docker pull mysql
    - docker run --name dev-mysql -e MYSQL_ROOT_PASSWORD=mummypapa -d mysql:latest
2.   Pull phpMyAdmin image and run inside container
    - docker pull arm64v8/phpmyadmin
    - docker run -d --name phpmyadmin-container -e PMA_HOST=host -e PMA_USER=shivi -e PMA_PASSWORD=mummypapa -p 8000:80 arm64v8/phpmyadmin
    - [docker run --name my-phpmyadmin -d -e PMA_HOST=your_mysql_host -p 8080:80 phpmyadmin/phpmyadmin]
3.  http://localhost:8080/index.php?route=/


                                                                                                                   


