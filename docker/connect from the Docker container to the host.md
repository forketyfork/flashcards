START
Basic
Front: How to connect from the Docker container to the host?
Back: 
When using Docker Desktop, you can use `host.docker.internal` domain name to connect to the host. However, in Docker CE (the engine typically installed on server), there's no such domain name. Instead, you can add the following to the `docker run` command: `--add-host host.docker.internal:host-gateway`
<!--ID: 1745138891623-->
END
