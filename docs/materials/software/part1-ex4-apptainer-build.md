---
status: testing
---

<style type="text/css">
  pre em { font-style: normal; background-color: yellow; }
  pre strong { font-style: normal; font-weight: bold; color: \#008; }
</style>

Software Exercise 1.4: Build, Test, and Deploy an Apptainer Container
====================================

**Objective**: to practice building and using a custom
apptainer container

**Why learn this?**: You may need to go through this process if you 
want to use a container for your jobs and can't find one that has 
what you need. 

Motivating Script
-----------------

1. Create a script called `cowsay.py`:

		:::file
		#!/usr/bin/python3

		import cowsay
		cowsay.cow('OSG User School')

1. Give it executable permissions: 

		:::console
		$ chmod +x cowsay.py

1. Try running the script:

		:::console
		$ ./cowsay.py

	It will likely fail, because the cowsay library isn't installed. 

Preparing a Definition File
---------------------------

	:::file
	Bootstrap: docker
	From: opensciencegrid/osgvo-ubuntu-20.04:latest

	%post
		apt-get update -y
		apt-get install -y \
				python3-pip \
				python3-cowsay
		python3 -m pip install numpy


This definition file installs a few packages from apt (that is,
Ubuntu prepared packages), and one package via pip. Using
package from the vendor is great as those packages are
generally well tested. However, not everything is packaged
by the OS vendors, and sometimes you need specific versions
of a package and then using language tools like pip, or 
building from source, can be good solutions.

The definition file above has two problems we have to
address before building. The first problem is that there
is no Ubuntu package for `python3-cowsay`. The second
problem (albeit minor), is that numpy might be better
installed with apt. The fix here is to swap and the names
of those two. Replace `python3-cowsay` with 
`python3-numpy` and replace `numpy` with `cowsay`.
The final definition file should look like:


``` file
Bootstrap: docker
From: opensciencegrid/osgvo-ubuntu-20.04:latest

%post
    apt-get update -y
    apt-get install -y \
            python3-pip \
            python3-numpy
    python3 -m pip install cowsay
```
## Testing the Image Locally

You can test the image on the access point by using
`singularity shell`. This will drop you in to the container, and
automatically mount $HOME so that you can access your files, which
is really nice when you have to test or build inside the container
environment, but want to keep the files after exiting the 
container. Run:

``` console
$ singularity shell first-image.sif
```

You should see the prompt change to indicate that you are inside
the container. Let's test our new container by starting Python,
import cowsay, and use the cowsay library:

``` console
Singularity> python3
Python 3.8.10 (default, Sep 28 2021, 16:10:42) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import cowsay
>>> cowsay.cow('Hello OSG User School!')
  ______________________
| Hello OSG User School! |
  ======================
                      \
                       \
                         ^__^
                         (oo)\_______
                         (__)\       )\/\
                             ||----w |
                             ||     ||
```

You can exit python and the container by pressing Ctrl-D
twice.




We then need a submit file - the only real differenc in this one
is the addition of `+SingularityImage` which specifies which image
to use:

```
+SingularityImage = "./first-image.sif"

request_cpus = 1
request_memory = 1GB
request_disk = 5GB

executable   = cowsay.py
output       = $(Cluster).$(Process).out
error        = $(Cluster).$(Process).err
log          = $(Cluster).log

queue 1
```

Run the job and verify the output. 






