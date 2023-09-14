# If process Pid1 is killed, container would crash (refer Kill_P1_process) . How to not loose the changes made?

Repeat steps in Kill_P1_process.md
1. Stop and remove the containers
    - docker stop [contianer_id]
    - docker rm [container_id]
2. Create a volumne in EC2
    - docker volume create demo
3. Map the volume created in EC2 with the volume in docker container
    - docker run -itd -p 82:80 demo:/var/www/html/ [image_id]
4. Enter into container
    - docker exec -it [container_id] bash
    - Make changes into file [/var/www/html/index.ngnix-debian.html]
    - vim /var/www/html/index.ngnix-debian.html
    - Restart ngnix
    - service nginx restart
5. ec2ip:port [Container would crash]
6. Creater the container from image
    - docker run -itd -p 82:80 -v demo:/var/www/html/ [image_id]
7. ec2ip:port

You can see the changes are not lost while container crashed.