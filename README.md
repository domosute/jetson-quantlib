# conda-quantlib
Jupyter Lab notebook with Quantlib Docker image for NVIDIA Jetson platform

- Used [docker-anaconda](https://hub.docker.com/r/continuumio/anaconda3) as a base image.
- [Quantlib](https://anaconda.org/domosute/quantlib-python) and [Quantlib-Python](https://anaconda.org/domosute/quantlib) are pulled from [here](https://anaconda.org/domosute/repo).
----
## Confirmed Environment
```

[root@xavier-NX ~]# cat /etc/nv_tegra_release
# R32 (release), REVISION: 6.1, GCID: 27863751, BOARD: t186ref, EABI: aarch64, DATE: Mon Jul 26 19:36:31 UTC 2021
[root@srv ~]# docker -v
Docker version 20.10.7, build 20.10.7-0ubuntu5~18.04.3
[root@srv ~]# docker-compose -v
docker-compose version 1.29.2, build unknown
```

## How to Run the Image
1. clone this repository.
```
[root@srv opt]# git clone https://github.com/domosute/jetson-quantlib.git
```
2. Enter the pulled directory and run `docker-compose` command to build.
```
[root@srv conda-quantlib]# docker-compose build
```
3. Once image is created run it.
```
[root@srv conda-quantlib]# docker-compose up -d
```
4. From browser, Access to `http://host:9999`.  Use `jupyter` as a password for the first time.
5. To stop the server, run the following.
```
[root@srv conda-quantlib]# docker-compose down
```
