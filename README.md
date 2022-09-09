# NavQ+ Containers
## Running

If you like to run the container use the following command and specify the appropriate volume mapping.

```
docker run -it --rm \
    -v /tmp/.X11-unix:/tmp/.X11-unix:ro \
    -e DISPLAY=${DISPLAY} \
    -e LOCAL_USER_ID="$(id -u)" \
    --name=container_name bperseghetti/navqplus-image-builder_lf5.15.32_2.0.0 /bin/bash
```

## Building

```
cd docker
docker build -f Dockerfile_navqplus_image_builder .
```
