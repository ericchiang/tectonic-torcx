# torcx-tectonic-bootstrap
Small agent to bootstrap a new Tectonic node.

## Background

When a new tectonic node is started in the cluster, it needs to have the correct
version of both the kubelet and corresponding docker torcx addons selected.

This is the first-boot equivalent to what the CLUO / NodeAgent do on a running
node.

## Process

1. Force an OS update
2. Determine the Kubelet version to install. 
3. Compute the correct Docker version.
4. Fetch the correct docker images
5. Set the correct kubelet version
6. Enable the real kubelet service

### Open design questions:
- What happens when an OS update fails?


## See also
[kube-version](https://github.com/coreos/kube-version)
