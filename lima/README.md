# Installation and troubleshooting with Lima-VM

This document provides steps to setup and troubleshoot Lima-VM x86_64 architecture on an ARM-based (MAC M1/M2) machines.

## Installation

´´´
$ brew install lima
$ brew install socket_vmnet
$ cp networks.yaml /Users/<Username>/.lima/_config/networks.yaml
$ mkdir -p ${HOMEBREW_PREFIX}/var/run
$ sudo ${HOMEBREW_PREFIX}/opt/socket_vmnet/bin/socket_vmnet --vmnet-gateway=192.168.105.1 ${HOMEBREW_PREFIX}/var/run/socket_vmnet
$ limactl start --name=ubuntu limavm.yaml
$ limactl shell ubuntu
´´´

The installation uses limavm.yaml and networks.yaml that are predifined to use VMNET on Ubuntu X86_64 image. Other configurations or distributions need different orchestration yamls. 
