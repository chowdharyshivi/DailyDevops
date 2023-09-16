# Launch multi-container app.
# docker-compose is a file by which we can launch multiple containers. It has the configs(service name, build, port, image, volumne etc) for the multiple containers. 
# repo - https://github.com/dockersamples/example-voting-app

1. Install docker-compose
    - sudo apt install docker-compose
2. git clone [repo http url]
3. Goto app folder
    - cd example-voting-app
4. It already has docker-compose-inages.yml file, launch multi -containers using this file
    - docker-compose -f [filename] up
5. Open ports for applications provided in the yml file.

