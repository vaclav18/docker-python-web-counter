# Docker Python web server counter get request

A Python based web server which returns a single integer which is incremented after each request

## Build the container
podman build . --tag counter

## Start the containter as root
podman run --name counter-test --detach counter

## List all running containers
podman ps

## Display containter's IP
podman inspect counter-test --format "{{.NetworkSettings.IPAddress}}"

## GET requests (prints counter's actual value)
curl [the above IP]:8080