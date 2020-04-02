# ros-dev-docker
ROS development environment in a Docker container.

## Quick start

##### Pull the docker image:
`docker pull cheymber/ros-dev-docker:dashing`

#####  Run the container:
`docker run -it cheymber/ros-dev-docker:dashing`
 
**OR** to start the container with a bind mount to your local project directory...

```
docker run \
    -it \
    --mount \
    type=bind,source=<local_project_directory>,target=<container_project_directory> \
    cheymber/ros2-dev-docker:dashing
```

This will allow changes made in the local_project_directory to be continuously synced with the container_project_directory. This sync is bi-directional as long as the container is running.
