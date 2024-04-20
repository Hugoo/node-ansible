# Secure

From: https://github.com/joelhans/ssdnodes-ansible-provision

1. Add host IP in /etc/ansible/hosts
2. Set user password in:

```
roles/user/tasks/main.yml
```

```sh
ansible-playbook -k provision.yml --ask-become-pass
```

Attention with IP table as the first init script adds a DROP ALL so then the iptable for erigon and stuff rules are going bellow than it is not working so the drop rule must be removed.
