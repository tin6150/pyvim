
# Singularity container definition for 
# pyvim -- vim with python
# stock centos  8 vim really
# https://github.com/tin6150/vim
# https://singularity-hub.org/collections/


BootStrap: docker
#From: centos:7.6.1810
#From: centos:7
From: centos:8

%help
	This container is a CentOS  with a fuller version of vim that supports python
  Pull and run via singularity hub:
	singularity pull --name pyvim shub://tin6150/pyvim
  ./pyvim

%runscript
	#echo "vim from inside the container..."
	/usr/bin/vim


%post
	#echo "Hello from inside the container"
	touch /THIS_IS_INSIDE_SINGULARITY
	#yum -ty update 
	#yum -ty install vim python2 zsh environment-modules
	dnf --assumeyes --quiet install vim python2 zsh environment-modules

	echo "end"                  >> /THIS_IS_INSIDE_SINGULARITY
	date                        >> /THIS_IS_INSIDE_SINGULARITY

%labels
MAINTAINER  Tin Ho tin'at'lbl.gov

