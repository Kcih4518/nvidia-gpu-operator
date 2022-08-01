# Ansible Role: Keepalived

[![CI](https://github.com/geerlingguy/ansible-role-haproxy/workflows/CI/badge.svg?event=push)](https://github.com/Kcih4518/nvidia-gpu-operator/actions?query=workflow%3ACI)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-gpu-blue.svg)](https://galaxy.ansible.com/kcih4518/nvidia_gpu_operator)

Helm installs Nvidia-GPU-operator for kubernetes on Ubuntu Linux servers.

**Note**: This role _officially_ supports Nvidia-GPU-operator versions v1.11.0.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    helm_bin_path: /usr/local/bin/helm
    pre_installed_gpu_drivers: true
    nfd_enable: true
    mig_strategy: mixed

## Example Playbook

    - hosts: kubernetes-master
      become: true
      roles:
        - { role: kcih4518.nvidia_gpu_operator }

## Author Information

This role was created in 2022 by [Avery Yang](https://www.linkedin.com/in/avery-yang-85b554144/).
