# Terraform working environment container

Contains specific software for a particular cloud provider such as for example GCE and terraform itself. Container is started as unprivileged user (specifically 1000:1000) if it differs from that what is used on your working machine then you might want to change it.


## GCE Terrafrom

Based on the latest [Google Cloud SDK Docker image](https://hub.docker.com/r/google/cloud-sdk/). Here's invocation example:

```
docker run --rm -it -v $HOME:/home/user -v $(pwd):/data dennybaa/terraform
```
