# sockperf-docker
A Docker image for [sockperf](https://github.com/Mellanox/sockperf).

This image uses the `sockperf` binary as the `ENTRYPOINT`, so any arguments you pass when running 
this container get passed straight through to `sockperf`.

## Running a UDP Ping-pong test
### On the server
```
docker run --rm -p 11111:11111/udp pazaan/sockperf sr
```

### On the client
```
docker run -it --rm pazaan/sockperf pp --ip <ip_address_of_docker_host> -m 64
```

If you're running on the local host, then `localhost` (ie, 127.0.0.1) will not work. Use the IP address 
of your machine on the LAN.

## Documentation
[Full documentation for sockperf](https://docs.nvidia.com/networking/pages/viewpage.action?pageId=19800142).

## GitHub repository
[GitHub repository for this Docker image](https://github.com/pazaan/sockperf-docker).

