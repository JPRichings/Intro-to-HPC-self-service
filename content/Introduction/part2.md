# How do HPC systems function?

From the HPC user perspective, the simulation process can be thought of as consisting of three linked steps: pre-processing, running of a simulation and post-processing.

## Pre-processing

The pre-processing stage takes care of the model settings and input data. Different simulations require different inputs - simple models do not require much input (e.g. a traffic model that we will introduce in the later weeks), but most of the useful simulations deal with a large amount of data. Usually, the input data comes from real-world observations, measurements and experiments. Let us take weather modelling as an example. How do you think numerical weather prediction works?
To make a forecast it is necessary to have a clear picture of the current state of the atmosphere and the Earth’s surface. Moreover, the quality of the forecast strongly depends on how well the numerical model can deal with all this information. Now, where do all these data points come from? They are gathered by various weather stations, satellite instruments, ships, buoys… and so on.
It’s not hard to imagine that all of these may record and store their measurements differently. That is why the pre-processing step is necessary - it prepares the data for further procedures, so that they can be easily and effectively used. This may mean simply making sure all the data is in the same format, and there are no invalid data entries, or performing more complicated operations such as removing noise from data, or normalising the data sets. The pre-processing stage ends when a simulation is ready to be launched.
## Execution

Quite often, especially on a large machines, once the simulation has been started it runs until the end or until a certain, significant point in a calculation (we call these checkpoints) has been reached, and only then the output is produced. We will talk about the batch submission procedure in later, but just to give you an idea of how it works - once a user submits their executable along with required input files to the submission queue, the job gets scheduled by a job scheduler, and some time later it runs and generates its output. In other words, you do not really see what is happening in the simulation and cannot interact with it.
There are a number of reasons why supercomputing facilities use this approach but the main ones are:

- A machine is a shared resource but most users want/need an exclusive access to the compute resources
- Most of the applications are written in a way that require dedicated resources to scale efficiently
- The whole system must be utilised as fully as possible (even during weekends and public holidays!) otherwise its resources are being wasted.
  
The point is that real-time visualisations (in situ visualisations), although slowly making their appearance, are not really used in a large scale simulations run on supercomputers. Downloading data to off-site locations (i.e. off the compute nodes of a supercomputer) allows interactive visualisations to be performed, without issues caused by limiting batch-mode workflows necessary on supercomputers. This means that to see what has happened during the simulation, i.e. to create a step-by-step visualisation of the simulation, it is necessary to save a lot of data at each time step.
Throughout the course we will be focusing on this step by running a number of simple exercises and examining how their performance changes depending on different problem and run settings.  


## Post-processing

The post-processing stage extracts the results of the simulation and puts them into a usable form. Initially, the typical output of any kind of simulation was simply a string of numbers, presented in a table or a matrix, and showing how different parameters changed during the simulations. However, humans are not very good at interpreting numbers. It is much easier to understand the results presented using graphs and animations, than to scan and interpret tables of numbers.
For example, in weather forecasting it is common to show the movement of rain or clouds over a map showing geographical coordinates and timestamps. Nowadays, it is common for the simulation outputs to graphically display large amounts of data.