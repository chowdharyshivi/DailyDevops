# Launch a server - Dockerfile, build image, Create container from image

1. Launch a EC2 instance
2. SSH into machine
3. Install docker ON Ubuntu -> https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04
4. docker ps -> see if any container is running
5. Create a docker file
    - vim Dockerfile
    - Add these steps to dockerfile:

      FROM ubuntu:latest
      ADD index.html .
      RUN apt-get update
      RUN apt-get install nginx -y
      EXPOSE 80
      CMD ["nginx","-g","daemon off;"]
6. Create a index.html file
    - touch index.html      
6. Build an image form the docker file
    - docker build .
7. List the images
    - docker images
8. Create a container from the image
    - docker run -itd -p [ec2port]:[containerport] image-id 
    - docker run -itd -p 81:80 image-id 
9. List all the containers
    - docker ps

Server has started, Goto EC2 instance > copy public ip > Open [public_ip]:port -> eg: 18.234.179.78:81


10. Go inside container and open bash shell
    - docker exec -it [contianer-id] bash  
11.       

      
