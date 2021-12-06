# W251 Rip Current Detection Project


This is a repo for our final project in W251 in the MIDS program. We attempt to detect riptides from video streams of the coast.

## Model Inference on the Cloud
1. Provision a `g4dn.2xlarge` instance on the cloud, using the Deep Learning AMI (Ubuntu 18.04) Version 52.0 as a base image. Expose port 22 for ssh
2. Ssh into the new instance on shell
3. Pull docker container:
```bash
docker pull rbector/w251-rip-current-project
```
4. Run docker container 
```bash
docker run -it --gpus all rbector/w251-rip-current-project
```
5. Start rip current detection program on the docker container, providing the appropriate input youtube stream.
```bash
python detect.py --source <youtube_stream_url> --weights best.pt --frames 90
```
6. Provide `riptide.detection@gmail.com` password and notificatione email when prompted.
