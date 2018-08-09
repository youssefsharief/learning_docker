Look at the commented out commands on the dockerfile and build this one first (by commenting out the second part). Then revert by commenting out the first and running the first part. Building and running the container is shown in the commands below

* docker build -t example/nanoer .
* docker run --rm -ti example/nanoer