
Notes based on https://www.youtube.com/watch?v=pEYjB5OIfqk 

docker pull ubuntu
`docker run -it ubuntu bash` which would allow you to use linux command line. To verify that, you could try the `ls` command
To exit from the bash `exit`
`docker ps`

Docker is ephemeral

* Notice that if you ran a docker and created a txt file by the following
    * Make sure docker is running in windows in the buttom right panel
    * `docker run -it ubuntu bash`
    * `echo "text content example" > text.txt`
    * `ls` to verify your txt file exists
    * `exit`
    * `docker run -it ubuntu bash`
    * `ls`, you should not file your created file
  
* Check container status
    * Try to have the docker container with linux running by `docker run -it ubuntu bash` command 
    * Open a new terminal and write `docker ps` 

* Create new container
    * Right now in our ubuntu a command like `wget` is not existant. You would need to install it in our ubuntu container
    * In order to automate this each time your run a container, you would need a Dockerfile
    * Look at the example of the dockerfile in branch `01`
    * This dockerfile represents a new container status. You would see the container we want to create is based on ubuntu
    * This example shows a container that is built on the basis on ubuntu but it further downloads packages that we need
    * You could build and run this container by using `docker build -t "name" .`
    * Now you could run your newly created container by `docker run -it "name" bash`
    * Now if you opened another terminal and checked the status through `docker ps`, you should find our container
        * Push your container to docker hub by `docker push`. This did not work with me
    * Concept of tags:
        * You could have a tag of latest like `docker pull mongo:latest`


* Use containers from other places
    * Go to `https://hub.docker.com/explore/`
    * `docker pull mongo`