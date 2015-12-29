# devstack-cinder-backup
Devstack with Cinder-Backup

Most of the documentation for setting devstack is there on openstack.org 
here are some quick steps 

# Prerequisites: 

 * DevStack setup requires to have 1 VM/ BM machine with internet connectivity.  

    Processor - at least 2 cores
    Memory - at least 8GB
    Hard Drive - at least 60GB

* Download the unbuntu image: https://help.ubuntu.com/community/Installation/MinimalCD

* Basics : Post installation run below basic packages and user details:

    $sudo apt-get install ssh

    where "stack" is any of your normal user.

    $useradd -m -G sudo  stack

    $ passwd stack

    $ usermod -s /bin/bash stack

    $sudo apt-get install git-core
    
# Steps:

 Clone devstack:
 
 $ git clone https://git.openstack.org/openstack-dev/devstack
 
 Clone devstack-cinder-backup

$ git clone https://github.com/poornimakshirsagar/devstack-cinder-backup/blob/master/local.conf

Copy the local.conf from to devstack

$ cp local.conf devstack/

Deploy your Devstack by running stack.sh
$cd devstack && ./stack.sh
