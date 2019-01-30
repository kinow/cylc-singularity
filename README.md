# Cylc Singularity Container

Example [singularity](https://www.sylabs.io/) container for [Cylc](https://cylc.github.io/cylc/).

See [this repository](https://github.com/kinow/cylc-docker) for Docker images.

## Creating the container for Cylc 7.8.1

    sudo singularity build cylc-7.8.1.simg Singularity-cylc-7.8.1

Once the command is done, you should have a binary called `cylc-7.8.1.simg`. You can
then execute Cylc with

	./cylc-7.8.1.simg check-software

Or even register suites, and run Cylc as you would normally run it. You can rename it to `cylc`
and store somewhere in your `$PATH`, without having to really install Cylc.

## Accessing the container

Assuming you have installed Singularity, try the following:

    singularity shell cylc-7.8.1.simg

That should give you a shell within the container.
