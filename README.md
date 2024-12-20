# Nachos-4.0 for Operating System Course 

## Before Starting Lab2

### Hint

Regardless of whether you have completed Lab1 or not, you must download this source code again.

If you find it too troublesome and you have already completed Lab1, you can simply download the "code" folder and overwrite the existing one.

In other words, if you haven't finished Lab1, it's fine - Lab2 is independent from Lab1.
## Docker

### Prerequisite(MacOS)

If you see `qemu: uncaught target signal 11 (Segmentation fault) - core dumped`, you may need to downgrade docker desktop to 4.24.2 or upgrade macos to Sonoma. See [here](https://github.com/docker/for-mac/issues/7172)

## VMware
You can reuse the virtual machine from Lab1, just need to git this repo.

### Build

```bash
# Download the source code if you haven't
git clone https://github.com/CYCU-CDLAB/2024-OperatingSystem-NachOS-Lab2.git nachos-lab2
cd nachos-lab2
# Build the docker image
# You can reuse the Docker image from Lab1.
docker build -t nachos .
```

### Run

Tested environments:

- Ubuntu
- MacOS

```bash
# Get into the directory if you are not in it
cd nachos-lab2
# Run the docker container with the source code mounted
docker run --rm -v $(pwd):/nachos -it --platform=linux/amd64 nachos

# Do not execute "bash build_nachos_docker.sh" or "bash build_nachos.sh" at first.
# There will be compilation errors (because the code in "threads" is not complete).
# You should execute "bash build_nachos_docker.sh" or "bash build_nachos.sh" after you have finished the code.
```


## Acknowledgment


This repository is based on LSA Lab, National Tsing Hua University.
