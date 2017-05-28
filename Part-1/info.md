# A brief explanation of containers

An *image* is a lightweight, stand-alone, executable package that include everything needed to run a
piece of software, including the code, a runtime, libraries, environment variables, and config
files.

A *container* is a runtime instance of an image - what the image becomes in memory when actually
executed. it runs completely isolated from the host environment by default, only accessing host
files and ports if configured to do so.

# Containers vs. virtual machines

*Virtual machines* run quest operating systems - OS layer in each machine. This is resource
intensive, and the resulting disk image and application state is an entanglement of OS settings,
system-installed dependencies, OS security patches, and other easy-to-lose, hard-to-replicate
ephemera.

*Containers* can share a single kernel, and the only information that needs to be in a container
image is the executable and its package dependencies, which never need to be installed on the host
system. These processes run live native processes, and you can manage them indicidually by running
commands like *docker ps*
