START
Basic
Front: Explain the EXPOSE instruction in the Dockerfile. How to expose tcp and/or udp ports? How to publish the exposed ports?
Back: 
- The `EXPOSE` instruction informs Docker that the container listens on the specified network port at runtime: `EXPOSE 80`
- By default, it assumes the tcp protocol, but you can publish udp as well: `EXPOSE 80/udp`. If you need to publish both, you need two lines.
- It doesn't actually publish the port, it's more of a contract between the one who builds the container and the one who runs it.
- To publish the port, you can use the `-p [host port]:[container port]` (`--publish`) argument of the `docker run` command or `-P` (`--publish-all`) to publish all exposed ports and map them to higher-order ephemeral ports.
- You can also use the `-p` argument to override whatever's exposed by the container, e.g.: `docker run -p 80:80/tcp -p 80:80/udp ...`
See [https://docs.docker.com/engine/reference/builder/#expose](https://docs.docker.com/engine/reference/builder/#expose)
<!--ID: 1745138891621-->
END
