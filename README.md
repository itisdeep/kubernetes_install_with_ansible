# Kubernetes Installation

This tutorial walks you through setting up Kubernetes Using ansible


## Target Audience

The target audience for this tutorial is someone who wants to understand the fundamentals of Kubernetes and how the core components fit together and then try its installation with Ansible.

## Labs
This tutorial requires four (4) AMD64 based virtual or physical machines connected to the same network. While AMD64 based machines are used for the tutorial, the lessons learned can be applied to other platforms.

The machine name can be changed in `playbooks/inventory.yaml` but for this excercise I have chosen the names below:

* admin-machine
* controller-0
* worker-0
* worker-1

Please set a user with name `ansible` which has sudo rights before starting this excercise.

Setup hostnames for each of the machines and update the inventory.yaml file with the set hostnames.

## Ansible roles
To install kubernetes with ansible, we use ansible galaxy in this tutorial and setup following roles for various stages.
* admin-machine
* compute-resources

## Execution
* Change the `inventory.yaml` file with the hostnames and ipaddresses for your setup.
* Under `admin-machine/files/machine.txt` update the entries accordingly as it will be used later to update the host entries on admin machines.
* Add the similar file under `compute-resources/files/` as these will be used later to update the host entries on Kubernetes cluster controller and worker nodes.
