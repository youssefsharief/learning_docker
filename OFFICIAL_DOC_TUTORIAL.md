* docker pull nginx
* `docker run --detach --publish 80:80 --name webserver nginx`
    * This command might not work in windows 10 so you would need to `netstat -a -n`. You could find that there is a port:80 listener which is blocking the docker
    * You could change the port to be 8080 but you would need to do the following if the container named webserver is running
        *  Stop a docker container `docker stop "name"` so you could use `docker stop "webserver"`
        *  Remove the container by `docker rm "name"` so you could use `docker rm webserver`
        *  The finally `docker run --detach --publish 8080:80 --name webserver nginx`
* Now if you visit localhost in the browser, you should find nginx initial page
* To see the only running containers
    * `docker container ls`
* To remove docker containers
    * docker container rm "names with spaces in between" (webserver laughing_kowalevski relaxed_sammet)

* Please use "cmder" for windows