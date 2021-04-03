# kata-env

Scripts to prepare kata runtime enviroment.

A `Vagrant` file for `k3s` deployment with `kata` `v1` runtime on `Fedora 33`.
Only `libvirt` provider is supported (tested).

The provisioning is done through an `Ansible` playbook. The deployment
might take 10-20 mins depending on time needed to pull images.
The environment is also verified with simple `http` server for the
`Ansible` playbook.

For the VM configuration look at [`Vagrantfile'](Vagrantfile)

# Prerequisites

- `Vagrant` with `libvirt` provider
- Tested on `Fedora 33` with `Vagrant 2.2.9`

# Usage

## Deployment
```
git clone https://github.com/jazik/kata-env.git
cd kata-env
vagrant up
```

## Access environment

```
vagrant ssh
```

The current configuration requires to be `root`:

```
sudo su -
kubectl get po -A
```

## Cleanup

```
vagrant destroy
```
