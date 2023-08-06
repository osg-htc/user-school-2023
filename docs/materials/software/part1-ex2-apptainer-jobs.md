---
status: in progress
---

<style type="text/css"> pre em { font-style: normal; background-color: yellow; } pre strong { font-style: normal; font-weight: bold; color: \#008; } </style>

Software Exercise 1.2: Use Apptainer Containers in OSPool Jobs
============================================================

Background
----------

Containers are another way to manage software installations. This guide shows how to use pre-existing containers to run jobs on the OSPool.

One caveat for using containers: not all systems will support them. HTCondor has built-in features for using Docker and many OSG resources have Singularity installed, but they are not always available everywhere. 

Setup
-----

Make sure you are logged into `login05.osgconnect.net` (the OSG Connect submit server for this workshop).  For this exercise we will be using Singularity containers that are hosted by OSG Connect. 


Default Environment
-------------------

First, let's run a job without a container to see what the typical job environment is. 

1. Create a bash script with the following lines: 

		:::bash
		#!/bin/bash
	
		hostname
		cat /etc/os-release 
		gcc --version
	
	This will print out the version of Linux on the computer and the version 
	of `gcc`, a common software compiler. 

1. Make the script executable: 
		:::something
		$ chmod +x script.sh

1. Run the script on the Access Point. 
		:::something
		$ ./script.sh
	What results did you get? 

1. Copy a submit file from a previous OSPool job and edit it so that the 
script you just wrote is the executable. 

1. Submit the job and read the standard output file when it completes. What version 
of Linux was used for the job? What is the version of `gcc`? 

Container Environment
---------------------

Now, let's try running that same script inside a container. 

1. For this job, we will use the OSG-provided Ubuntu "Focal" image. The `container_image` submit file option will tell HTCondor to use this container: 

		:::file
		universe = container
		container_image = /cvmfs/singularity.opensciencegrid.org/opensciencegrid/osgvo-ubuntu-20.04:latest

1. Submit the job and read the standard output file when it completes. 
What version of Linux was used for the job? What is the version of `gcc`? 

Experimenting With Other Containers
-------------

1. Look at the list of OSG-Supported containers: [OSG Supported Containers](https://portal.osg-htc.org/documentation/htc_workloads/using_software/available-containers-list/)

1. Try submitting a job that uses one of these containers. Change the executable 
script to explore different aspects of that container. 
