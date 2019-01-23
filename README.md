# [LAB] microk8s with pod security policies

## Introduction

This laboratory is developed to have a first contact with the [`Pod Security Policies`](https://kubernetes.io/docs/concepts/policy/pod-security-policy/) locally using [`microk8s`](https://microk8s.io/).

## LAB assumptions and requirements

This lab assumes you have basic knowledge about [kubernetes](https://kubernetes.io/), [RBAC](https://en.wikipedia.org/wiki/Role-based_access_control) and basic linux commands and concepts.
As a requirement, you must have installed [*(default installation)* `microk8s`](https://microk8s.io/docs/) on your linux PC. Then enable the `dns` microk8s plugin: `microk8s.enable dns`.

To check that `microk8s` is running correctly, execute the following command, you should have an output like the one shown below:

```bash
$ sudo microk8s.inspect
Inspecting services
  Service snap.microk8s.daemon-docker is running
  Service snap.microk8s.daemon-apiserver is running
  Service snap.microk8s.daemon-proxy is running
  Service snap.microk8s.daemon-kubelet is running
  Service snap.microk8s.daemon-scheduler is running
  Service snap.microk8s.daemon-controller-manager is running
  Service snap.microk8s.daemon-etcd is running
  Copy service arguments to the final report tarball
Inspecting AppArmor configuration
Gathering system info
  Copy network configuration to the final report tarball
  Copy processes list to the final report tarball
  Copy snap list to the final report tarball
  Inspect kubernetes cluster

Building the report tarball
  Report tarball is at /var/snap/microk8s/383/inspection-report-20190123_110858.tar.gz
```

## Guide

- [0. Save default kubeconfig](./0.Default-kubeconfig.md)
- [1. Configure RBAC](./1.Configure-RBAC.md)
- [2. Create a cluster-admin kubeconfig file](./2.Create-cluster-admin-kubeconfig.md)