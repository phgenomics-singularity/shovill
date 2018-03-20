# shovill

A shovill singularity recipe

Singularity container for Torsten Seemann's [SHOVILL](https://github.com/tseemann/shovill)

## Pre-requisite

Install [Singularity](http://singularity.lbl.gov/docs-installation)

## Usage

### Latest version

The following steps are needed to use the image:

1. Pull the image:

```
singularity pull --name shovill shub://phgenomics-singularity/shovill@latest
```
This will command will create a file `shovill.simg`, which is executable.

2. Use the image:
```
./shovill.simg --help
```

### A particular version

```
singularity pull --name shovill shub://phgenomics-singularity/shovill@v0.9.0
```

## Suggested pattern

1. Create a `singularity` folder:

```
mkdir $HOME/singularity
```

2. Pull the image to the `singularity` folder.

```
singularity pull --name shovill_v0.9.0 shub://phgenomics-singularity/shovill@v0.9.0
```

3. Link the image to a folder in your `$PATH` (e.g., `$HOME/bin`)

```
ln -s $HOME/singularity/shovill_v0.9.0.simg $HOME/bin/shovill
```

Now, when you login again, you should be able to just type:

```
shovill --help
```
