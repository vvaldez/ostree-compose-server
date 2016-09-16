# ostree-compose-server
The goal of this playbook is to setup a compose server, build a custom tree, then add this compose server as a remote to atomic clients and rebase to the tree.

# prerequisites
* The compose server should have access to rpm-ostree and git rpms and have the /srv directory served out via http
* The clients should be booted into a version of atomic host
* The playbook expects to point to a local repo for content which should be setup with creatrep and exported via http (These tasks can be commented out to use the online mirrorlist instead)

# executing
Edit the hosts file to make sure it matches your environment and run it as such:
```
ansible-playbook -i hosts custom-ostree-server.yml
```

