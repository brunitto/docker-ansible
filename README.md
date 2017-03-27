# DOCKER ANSIBLE

A simple Docker image to run Ansible.

## Compability

This image was created from `debian:latest` and installs the latest Ansible
version available at PPA.

## Usage

Change the working directory to your playbooks directory and execute:

    $ docker run --rm -v "$(pwd):/src" brunitto/ansible

It's also a good idea to copy your SSH private keys to the container:

    $ docker run --rm -v "$(pwd):/src" -v "~/.ssh/id_rsa:/root/.ssh/id_rsa brunitto/ansible

This image use `CMD ["bash"]` in the Dockerfile to start the container with a
bash session. As the entrypoint for `debian` image is `/bin/sh -c`, the
container ends up with `/bin/sh -c bash`.

## Issues

[Report issues at GitHub](https://github.com/brunitto/docker-ansible/issues)

## Contribute

[Check the official repository at GitHub](https://github.com/brunitto/docker-ansible)
