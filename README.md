# Ansible K3s Cluster Setup (Raspberry Pi)
[![Ansible](https://img.shields.io/badge/ansible-automation-blue.svg?logo=ansible)](https://www.ansible.com/)
[![K3s](https://img.shields.io/badge/k3s-lightweight%20kubernetes-orange.svg?logo=kubernetes)](https://k3s.io/)
[![Cilium](https://img.shields.io/badge/cni-cilium-66C2A5.svg?logo=linux)](https://cilium.io/)

[![CI](https://github.com/sfotiadis/ansible-rpi-cluster/actions/workflows/ci.yml/badge.svg)](https://github.com/sfotiadis/ansible-rpi-cluster/actions/workflows/ci.yml)


This repository contains the Ansible automation to install and manage a lightweight **K3s Kubernetes cluster** on Raspberry Pis.  
The cluster uses **Cilium** as the CNI and is designed to be GitOps-ready with Flux.

For the GitOps configuration itself, see the companion repository [sfotiadis/flux-rpi-cluster](https://github.com/sfotiadis/flux-rpi-cluster).

---

## Features
- Automated installation of **K3s master** and **worker nodes**
- Secure handling of cluster IPs via **Ansible Vault**
- Automatic retrieval of the **k3s join token** from the master node
- Installation of **Cilium CNI** and **Hubble observability**
- Ready for GitOps with [**sfotiadis/flux-rpi-cluster**](https://github.com/sfotiadis/flux-rpi-cluster)

---

## Prerequisites
Install Ansible:
```bash
sudo apt update
sudo apt install ansible -y
```

## Run Cluster Setup
```bash
ansible-playbook playbooks/site.yml --ask-vault-pass
```
