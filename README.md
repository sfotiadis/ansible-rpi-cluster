# Ansible K3s Cluster Setup (Raspberry Pi)
[![Ansible](https://img.shields.io/badge/ansible-blue.svg?logo=ansible)](https://www.ansible.com/)
[![K3s](https://img.shields.io/badge/k3s-black.svg?logo=k3s)](https://k3s.io/)
[![Cilium](https://img.shields.io/badge/cilium-white.svg?logo=cilium)](https://cilium.io/)

[![CI](https://github.com/sfotiadis/ansible-rpi-cluster/actions/workflows/ci.yml/badge.svg)](https://github.com/sfotiadis/ansible-rpi-cluster/actions/workflows/ci.yml)


This repository contains the Ansible automation to install and manage a lightweight **K3s Kubernetes cluster** on Raspberry Pis.  
The cluster uses **Cilium** as the CNI and is designed to be GitOps-ready with Flux.

For the GitOps configuration itself, see the companion repository [sfotiadis/flux-rpi-cluster](https://github.com/sfotiadis/flux-rpi-cluster).

---

## Features
- Automated installation of **K3s master** and **worker nodes**
- Secure handling of sensible data via **Ansible Vault**
- Automatic retrieval of the **k3s join token** from the master node
- Installation of **Cilium**
- Kubernetes secret creation to store SOPS GPG key in the cluster
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
