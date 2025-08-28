# Ansible K3s Cluster Setup (Raspberry Pi)

This repository contains the Ansible automation to install and manage a lightweight **K3s Kubernetes cluster** on Raspberry Pis.  
The cluster uses **Cilium** as the CNI and is designed to be GitOps-ready with Flux.

---

## Features
- Automated installation of **K3s master** and **worker nodes**
- Secure handling of cluster IPs via **Ansible Vault**
- Automatic retrieval of the **k3s join token** from the master node
- Installation of **Cilium CNI** and **Hubble observability**

---

## Structure
ansible-rpi-cluster/
├── inventories/
├── playbooks/
├── roles/
└── README.md
