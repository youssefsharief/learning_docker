* docker pull node
* docker run --rm -it node bash
    * Adding a js inside docker
        * To copy a file from your PC to the container:
            * Use `docker cp "filename" "container name":/"filename"`
                * Notie that container name is not "node" in this case. Node is the image type

    * Run this file using `node index.js`
    * 