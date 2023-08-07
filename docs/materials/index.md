
# OSG School Materials

## School Overview and Intro

<!-- View the slides
([PDF](files/osgvsp21-overview.pdf),
[PowerPoint](files/osgvsp21-overview.pptx))
-->

## Intro to HTC and HTCondor Job Execution

### Intro to HTC Slides

Intro to HTC: [PDF](htcondor/files/osgus23-intro-to-htc.pdf)
Worksheet: [PDF](htcondor/files/osgus23-htc-worksheet.pdf)

### Intro to HTCondor Slides

View the slides
([PDF](htcondor/files/osgus23-htc-htcondor.pdf))
<!--
[PowerPoint](htcondor/files/osgus22-htc-htcondor.pptx))
-->

### Intro Exercises 1: Running and Viewing Simple Jobs (Strongly Recommended)

- [Exercise 1.1: Log in to the local submit machine and look around](htcondor/part1-ex1-login)
- [Exercise 1.2: Experiment with HTCondor commands](htcondor/part1-ex2-commands.md)
- [Exercise 1.3: Run jobs!](htcondor/part1-ex3-jobs.md)
- [Exercise 1.4: Read and interpret log files](htcondor/part1-ex4-logs.md)
- [Exercise 1.5: Determining Resource Needs](htcondor/part1-ex5-request.md)
- [Exercise 1.6: Remove jobs from the queue](htcondor/part1-ex6-remove.md)

### Bonus Exercises: Job Attributes and Handling

- [Bonus Exercise 1.7: Compile and run some C code](htcondor/part1-ex7-compile.md)
- [Bonus Exercise 1.8: Explore `condor_q`](htcondor/part1-ex8-queue.md)
- [Bonus Exercise 1.9: Explore `condor_status`](htcondor/part1-ex9-status.md)

## Intro to HTCondor Multiple Job Execution

Slides coming soon. 
<!--
View the Slides ([PDF](htcondor/files/osgus22-htc-htcondor-PART2.pdf))
-->

### Intro Exercises 2: Running Many HTC Jobs (Strongly Recommended)

- [Exercise 2.1: Work with input and output files](htcondor/part2-ex1-files.md)
- [Exercise 2.2: Use `queue N`, `$(Cluster)`, and `$(Process)`](htcondor/part2-ex2-queue-n.md)
- [Exercise 2.3: Use `queue from` with custom variables](htcondor/part2-ex3-queue-from.md)
- [Bonus Exercise 2.4: Use `queue matching` with a custom variable](htcondor/part2-ex4-queue-matching.md)


## OSG

Slides coming soon!

<!--
View the slides
([PDF](osg/files/osgvs21-day3-osg.pdf),
[PowerPoint](osg/files/osgvs21-day3-osg.pptx))
-->

<!--
### OSG Exercises: Comparing CHTC and OSG (Strongly Recommended)

- [Exercise 1.1: Refresher – submitting multiple jobs](osg/part1-ex1-submit-refresher.md)
- [Exercise 1.2: Log in to the OS Pool Access Point](osg/part1-ex2-login-scp.md)
- [Exercise 1.3: Running jobs in OSG](osg/part1-ex3-submit-osg.md)
- [Exercise 1.4: Hardware differences between CHTC and OSG](osg/part1-ex4-hardware-diffs.md)
- [Exercise 1.5: Software differences in OSG](osg/part1-ex5-software-diffs.md)

-->

## Troubleshooting

([PDF](troubleshooting/files/osgus22-htc-troubleshooting.pdf),
[PowerPoint](troubleshooting/files/osgus22-htc-troubleshooting.pptx))

### Troubleshooting Exercises: 

- [Exercise 1.1: Troubleshooting Jobs](troubleshooting/part1-ex1-troubleshooting.md)
- [Exercise 1.2: Job Retry](troubleshooting/part1-ex2-job-retry.md)

## Software

Slides will be posted here

### Software Exercises 1: Exploring Containers

- [Exercise 1.1: Run and Explore Apptainer Containers](software/part1-ex1-run-apptainer.md)
- [Exercise 1.2: Use Apptainer Containers in OSPool Jobs](software/part1-ex2-apptainer-jobs.md)
- [Exercise 1.3: Use Docker Containers in OSPool Jobs](software/part1-ex3-docker-jobs.md)
- [Exercise 1.4: Build, Test, and Deploy an Apptainer Container](software/part1-ex4-apptainer-build.md)
- [Exercise 1.5: Choose Software Options](software/part1-ex5-pick-an-option.md)

### Software Exercises 2: Preparing Scripts
- [Exercise 2.1: Build an HTC-Friendly Executable](software/part2-ex1-build-executable.md)

### Software Exercises 3: Container Examples

- [Exercise 3.1: Create an Apptainer Definition File (Optional)](software/part3-ex1-apptainer-recipes.md)
- [Exercise 3.2: Build Your Own Docker Container (Optional)](software/part3-ex2-docker-build.md)

### Software Exercises 4: Exploring Compiled Software

- [Exercise 3.1: Download and Use Compiled Software](software/part4-ex1-download.md)
- [Exercise 3.2: Use a Wrapper Script To Run Software](software/part4-ex2-wrapper.md)
- [Exercise 1.3: Using Arguments With Wrapper Scripts](software/part4-ex3-arguments.md)

### Software Exercises 5: Compiled Software Examples 

- [Exercise 4.1: Compiling a Research Software](software/part5-ex1-prepackaged.md)
- [Exercise 4.2: Compiling Python and Running Jobs](software/part5-ex2-python.md)
- [Exercise 4.3: Using Conda Environments](software/part5-ex3-conda.md)
- [Exercise 4.4: Compiling and Running a Simple Code](software/part5-ex4-compiling.md)


## Data

View the slides
([PDF](data/files/osgus23-data.pdf),
[PowerPoint](data/files/osgus23-data.pptx))

### Data Exercises 1: HTCondor File Transfer (Strongly Recommended)

- [Exercise 1.1: Understanding a job's data needs](data/part1-ex1-data-needs.md)
- [Exercise 1.2: transfer\_input\_files, transfer\_output\_files, and remaps](data/part1-ex2-file-transfer.md)
- [Exercise 1.3: Splitting input](data/part1-ex3-blast-split.md)

### Data Exercises 2: Using OSDF (Strongly Recommended)

- [Exercise 2.1: OSDF for inputs](data/part2-ex1-osdf-inputs.md)
- [Exercise 2.2: OSDF for outputs](data/part2-ex2-osdf-outputs.md)

## Workflows with DAGMan

View the slides
([PDF](data/files/osgus23-dagman.pdf),
[PowerPoint](data/files/osgus23-dagman.pptx))

### DAGMan Exercises 1

- [Exercise 1.1: Coordinating set of jobs: A simple DAG](workflows/part1-ex1-simple-dag.md)
- [Exercise 1.2: A brief detour through the Mandelbrot set](workflows/part1-ex2-mandelbrot.md)
- [Exercise 1.3: A more complex DAG](workflows/part1-ex3-complex-dag.md)
- [Exercise 1.4: Handling jobs that fail with DAGMan](workflows/part1-ex4-failed-dag.md)
- [Bonus Exercise 4.5: HTCondor challenges](workflows/part1-ex5-challenges.md)

## Extra Topics

<!-- BEGIN EXTRA TOPICS THAT ARE NOT READY YET


### Containers (and GPUs?)

View the slides
([PDF](gpus/files/osgvsp21-gpus-containers.pdf),
[PowerPoint](gpus/files/osgvsp21-gpus-containers.pptx))

- [Exercise 1.1: Containers Overview](gpus/part1-ex1-containers-overview.md)
- [Exercise 1.2: Running a CPU job](gpus/part1-ex2-cpu-jobs.md)
- [Exercise 1.3: Running a GPU job](gpus/part1-ex3-gpu-jobs.md)

END EXTRA TOPICS THAT ARE NOT READY YET -->

### Self-checkpointing for long-running jobs

View the **DRAFT** slides
([PDF](checkpoint/files/osgus22-day5-1-selfcheckpointing-DRAFT-20220720.pdf))

-   [Exercise 1.1: **DRAFT**: Trying out self-checkpointing](checkpoint/part1-ex1-checkpointing.md)

<!-- BEGIN EXTRA TOPICS THAT ARE NOT READY YET

### Introduction to Research Computing Facilitation

Slides will be posted here.

END EXTRA TOPICS THAT ARE NOT READY YET -->

