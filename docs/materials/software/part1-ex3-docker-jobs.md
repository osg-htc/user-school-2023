---
status: in progress
---

<style type="text/css"> pre em { font-style: normal; background-color: yellow; } pre strong { font-style: normal; font-weight: bold; color: #008; } </style>

Software Exercise 1.3: Use Docker Containers in OSPool Jobs
====================================

**Objective**: Submit a job that uses an existing Docker container. 

**Why learn this?**: Same as the previous exercise; this may also be how you end up 
submitting your jobs if you can find an existing Docker container with your software.  

Submit File and Executable
-------------------

1.  Make a copy of your submit file from the [previous container exercise](../part1-ex2-apptainer-jobs) or build from an existing submit file. 

1.  Add the following lines to the submit file or modify existing lines to match the lines below: 

		:::file
		universe = container
		container_image = docker://python:3.10

	Here we are requesting HTCondor's Docker universe and using a pre-built python image that, by default, will be pulled from a public website of Docker images called DockerHub.  

1.  Use the same executable as the [previous exercise](../part1-ex2-apptainer-jobs). 

1. Once these steps are done, submit the job.

Finding Docker Containers
-------------

There are a lot of Docker containers on Docker Hub, but they are not all 
created equal. Anyone can create an account on Docker Hub and share container images there, so it’s important to exercise caution when choosing a container image on Docker Hub. These are some indicators that a container image on Docker Hub is consistently maintained, functional and secure:

- The container image is updated regularly.
- The container image is associated with a well established company, community, or other group that is well-known.
- There is a Dockerfile or other listing of what has been installed to the container image.
- The container image page has documentation on how to use the container image. [^1]

1. Can you find a container on [Docker Hub](https://hub.docker.com/) that would be 
useful for running Jupyter notebooks that use tensorflow? 

1. Does your chosen image meet at least 2 of the criteria above? 

[^1]: This list and previous text taken from [Introduction to Docker](https://carpentries-incubator.github.io/docker-introduction/)