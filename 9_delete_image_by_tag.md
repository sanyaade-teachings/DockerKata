# Delete Image by Tag

Docker Documentation References:

[docker rmi](https://docs.docker.com/engine/reference/commandline/rmi/)

[docker images](https://docs.docker.com/engine/reference/commandline/images/)

### Intent

The purpose of this kata is to familarize yourself with the process of deleting an image from your local docker registry using a tag to select a specific image.

### Overview

In this exercies we will list the images on in the local registry and then delete one using a tag to identify the image.

### Kata Steps

1 List Images

**Command:**

```bash
docker images
```

**Output:**

```bash
thought:DockerKata rich$ docker images
REPOSITORY                                   TAG                 IMAGE ID            CREATED             SIZE
nginx                                        alpine              f00ab1b3ac6d        2 weeks ago         15.5 MB
nginx                                        mine                f00ab1b3ac6d        2 weeks ago         15.5 MB
```

2 Remove image

**Command:**

```bash
docker rmi nginx:mine
```

> Note: We use the IMAGE ID for the listed image to select which image to delete

**Output:**

```bash
thought:DockerKata rich$ docker rmi nginx:mine
Untagged: nginx:mine
```

3 List Images

**Command:**

```bash
docker images
```

**Output:**

```bash
thought:DockerKata rich$ docker images
REPOSITORY                                   TAG                 IMAGE ID            CREATED             SIZE
nginx                                        alpine              f00ab1b3ac6d        2 weeks ago         15.5 MB
```

[Previous](8_tag_an_image.md) | [Index](README.md) | [Next](#)