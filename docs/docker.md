# Docker Images

The Micro-Epsilon scanCONTROL repository provides a [Dockerfile](`./docker/Dockerfile) that can be used to create
a Docker container which has the scanCONTROL SDK installed. By default it target ROS 2 Jazzy on Ubuntu 24.04 (Noble).

### Arguments
The DOCKERFILE allows the following arguments:
- `SCANCONTROL_SDK_VERSION` (`default="1.0.0"`)
- `UBUNTU_VERSION` (`default="24.04"`)
- `ROS_DISTRO` (`default="jazzy"`)

The `SCANCONTROL_SDK_VERSION` is used to download 
## Build the containers

To build the standard container:
```bash
docker build . -t samxl/scancontrol:jazzy-sdk_v1.0.0[-YYYYMMDD]
```

Alternatively, the container can also be build for `ROS 2 Humble` and `Ubuntu 22.04`
```bash
docker build . -t samxl/scancontrol:humble-sdk_v1.0.0[-YYYYMMDD] --build-arg UBUNTU_VERSION=22.04 --build-arg ROS_DISTRO=humble
```

The `UBUNTU_VERSION` is used to build and package the scanCONTROL SDK, while the `ROS_DISTRO` is 