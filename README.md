# albuild-snap

A set of prebuilt snapd and snap tools for Amazon Linux 2.

## Install (Amazon WorkSpaces)

### Instructions

1. Download the snap-confine and snapd packages from [the Release page](https://github.com/albuild/snap/releases/tag/v0.1.0).

1. Install the package.

    ```
    sudo yum -y install snap-confine-0.1.0-0.amzn2.x86_64.rpm snapd-0.1.0-0.amzn2.x86_64.rpm
    ```

1. Enable the snapd.socket.

    ```
    sudo systemctl enable --now snapd.socket
    ```

1. Logout and login.

## Build (Amazon WorkSpaces)

### System Requirements

* Docker

### Instructions

1. Clone this repository.

    ```
    git clone https://github.com/albuild/snap.git
    ```

1. Go to the repository.

    ```
    cd snap
    ```

1. Build a new image.

    ```
    bin/build
    ```

1. Extract built packages from the built image. The packages will be copied to the ./rpm directory.

    ```
    bin/cp
    ```

1. Delete the built image.

    ```
    bin/rmi
    ```
