# Singularity configuration for simg-rnaseqvariants2 container

A [Singularity](http://singularity.lbl.gov) definition for rnaseqvariants2 workflow, available at [https://www.singularity-hub.org/collections/2532](https://www.singularity-hub.org/collections/2532).

If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-rnaseqvariants2.simg Singularity > build.log 2>&1
```

The container can also be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-rnaseqvariants2.simg" sschmeier/simg-rnaseqvariants2
```

Then, it can be used, e.g.:

```bash
singularity exec simg-rnaseqvariants2.simg opossum --help
```
