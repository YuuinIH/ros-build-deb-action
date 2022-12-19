# ros-build-deb-action
[![Test](https://github.com/gdut-dynamic-x/ros-build-deb-action/actions/workflows/test.yml/badge.svg)](https://github.com/gdut-dynamic-x/ros-build-deb-action/actions/workflows/test.yml)

Build debian packages from ROS 1 packages using Github Action.

# Usage
See [action.yml](action.yml).

## Basic
```yaml
container: 
  image: ros:noetic
steps:
    - uses: actions/checkout@v3
    - uses: gdut-dynamic-x/ros-build-deb-action@v1
      with:
        ros_distro: noetic
        timestamp: true
    - name: Get artifact
      uses: actions/upload-artifact@v3
      with:
        name: artifact
        path: |
            *.deb
            *.ddeb
```

# License
The scripts and documentation in this project are released under the [MIT License](LICENSE)