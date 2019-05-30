Bootstrap: docker
From: oraclelinux:7

%help
    This is a demo image to test CernVM-FS deployment on ITS resources

%labels
    Author Nicholas Schiraldi


%environment
    export SINGULARITY_BIND="/network:/network"
    export LANG=C.UTF-8 
    LC_ALL=C.UTF-8

%post 
    yum -y update && yum -y install https://ecsft.cern.ch/dist/cvmfs/cvmfs-release/cvmfs-release-latest.noarch.rpm
