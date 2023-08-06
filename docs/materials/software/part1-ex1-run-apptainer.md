---
status: in progress
---

<style type="text/css"> pre em { font-style: normal; background-color: yellow; } pre strong { font-style: normal; font-weight: bold; color: \#008; } </style>

Software Exercise 1.1: Run and Explore Containers
============================================================

**Objective**: Run a container interactively

**Why learn this?**: Being able to run a container directly allows you to confirm 
what is installed and whether any additional scripts or code will work in the context 
of the container. 

Setup
--------

Make sure you are logged into `ap40.uw.osg-htc.org`.  For this exercise 
we will be using Apptainer containers maintained by OSG staff or existing 
containers on Docker Hub. 

We will set two environment variables that will help lighten the load on the 
Access Point as we work with containers: 

	:::console
	$ mkdir ~/apptainer_cache
	$ export APPTAINER_CACHEDIR=$HOME/apptainer_cache
	$ export TMPDIR=$HOME/apptainer_cache

Exploring Apptainer Containers
-------------------

https://portal.osg-htc.org/documentation/htc_workloads/using_software/available-containers-list/

/cvmfs/singularity.opensciencegrid.org/opensciencegrid/osgvo-ubuntu-20.04:latest



Exploring Docker Containers
------------------

The process for interactively running a Docker container will be very 
similar to an apptainer container. The main difference is a `docker://` prefix 
before the container's identifying name. 

1. 

python:3.10

