# Template for running ROS 2 projects in docker containers

This is a plain ROS2 containerized using docker.


## Docker setup and instructions:

Make sure docker is set up and nvidia-container-toolkit is installed.

Adjust the `env` file:
- Project name
- Data directory (placement on local/host pc)
- Output data directory (placement on local/host pc)


```bash
docker compose build dev
docker compose up dev
docker exec -it $name_of_container bash
```


## Submodules:
Clone the repo with submodules:
```bash
git clone --recursive git@github.com:Lucasmogsan/ROS2_docker_template.git
```

Alternatively clone the repo and then get the submodules afterwards:

```bash
git clone git@github.com:Lucasmogsan/ROS2_docker_template.git
```

```bash
git submodule update --init --recursive
```


The main repo has references to the submodules. If these submodules are modified, then the main repo may need to update these references in order to pull the latest data.
```bash
git submodule update --remote
```

This modifies the references in the main repo, and these changes needs to be comitted and pushed.


## Useful ROS commands

TBC...

```bash
ros2 bag info <bag_file_name>
ros2 bag play <bag_file_name>
```