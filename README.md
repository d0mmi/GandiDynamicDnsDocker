# GandiDynamicDnsDocker

This repository builds a Docker image for the [GandiDynamicDns](https://github.com/Aldaviva/GandiDynamicDns) project. The GandiDynamicDns tool allows you to update Gandi LiveDNS records dynamically based on your current IP address.

## Docker Image

The prebuilt Docker images for this project are available on Docker Hub:  
[https://hub.docker.com/r/d0mmi/gandidynamicdns](https://hub.docker.com/r/d0mmi/gandidynamicdns)

## Usage

To use the Docker image, pull it from Docker Hub:

```
services:
  gandidynamicdns:
    image: d0mmi/gandidynamicdns:latest
    volumes:
      - ./appsettings.json:/app/appsettings.json
```


Replace `gandiApiKey`, `domain`, and `subdomain` in the appsettings.json with your Gandi API key, domain, and DNS record, respectively.

## Building the Image Locally

If you prefer to build the Docker image locally, clone this repository and run:

```bash
services:
  gandidynamicdns:
    build: ./linux64
    volumes:
      - ./appsettings.json:/app/appsettings.json
```

For arm you can use `./arm` or `./arm64`

## License

This project is licensed under the same terms as the [GandiDynamicDns](https://github.com/Aldaviva/GandiDynamicDns) repository. Please refer to their repository for more details.

## Acknowledgments

Special thanks to [Aldaviva](https://github.com/Aldaviva) for creating the original GandiDynamicDns project.