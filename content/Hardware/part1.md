# The key hardwar of HPC systems

Before we can use a HPC system effectively we should first understand the key components of such systems and how they compare to other computers we might be more familer with.

## Nodes

A HPC system can inveritably be described as a collection of nodes. Each node contains the same components as a standard workstation or laptop.

- We have a CPU and some memory, as well as a power supply, cooling and a network connection. These nodes downt nessisarily have a data storage disk but will have access to a file system for storing files that is accesible over the netwrork. 
- These components are often very similar to what you find in your laptop as the market for consumer electronics is much larger than for HPC systems research and development in computing is focused on that market and HPC systems then tend to be built for these components.
- 

### CPU

- Central processing unit

- What is actually doing calculations.


#### Intel

- image of the intel CPU
- list some key characteristics of these processors.
- Notes on performance characteristics.


#### AMD

- image of the AMD CPU
- list some key characteristics of these processors.
- Notes on performance characteristics.

#### ARM

- image of the ARM CPU
- list some key characteristics of these processors.
- Notes on performance characteristics.

### Memory

Memory in a compute nodes is orginised in a hierarchy to smooth memory access.

#### RAM

- Larger but slower

#### Cache

- Quick but small

## Interconnect 

What defines a super computer is the ability to get all of the compute nodes to talk to each other and work to gether to perform a calculation.

- Each node has conenctions to a network which links all the nodes together the nodes are connected via switches.

### Switches 



### Topology

The network of a HPC can be orginised in a variety of ways to optimise the pattern of communcation for the applications that will use the system.

There are a number of common topologies:

- Fat tree
- Dragonfly
- hypercudic

The main thing to consider is the type of communication pattern 


## File system

File systems are where your data is stored ...

### Lustre


## Accelerators

It is becoming more common for hpc systems to include accelerators in order to increase the avalible compute performance of the system.

Accelerators are 


### Nvidia

### AMD

### Intel
