[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/3075)


# singularity

A collection of singularity images that may be useful for HPC

## cernvmfs
This image allows rootless integration of /cvmfs/ on any machine with singularity installed. Please see https://cernvm.cern.ch/portal/filesystem/parrot for more information on the parrot connector.

Note, that in the example we are binding a local /network/ directory to /network/ on the image, to expose NFS shares. 
```bash
$ singularity pull shub://nschiraldi/singularity:cernvmfs
$ singularity exec --bind /network/:/network/ singularity_cernvmfs.sif parrot_run bash --noprofile --norc Singularity> cd /cvmfs/alice.cern.ch
Singularity> ls
LibCvmfs version 2.4, revision 25
bin          el5-x86_64  etc                x86_64-2.6-gnu-4.1.2  x86_64-2.6-gnu-4.8.4
calibration  el6-x86_64  ubuntu1404-x86_64  x86_64-2.6-gnu-4.7.2
data         el7-x86_64  ubuntu1604-x86_64  x86_64-2.6-gnu-4.8.3
```
