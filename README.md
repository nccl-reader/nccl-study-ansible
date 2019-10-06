# Ansible playbooks for nccl-study0*

## How to use
```
ansible-playbook -i hosts playbooks/xxxx.yml -K
```

## How to build NCCL on all nodes
0. Edit `playbooks/mynccl.yml` to fit your own config
```
  vars:
    - username: enp1s0
    - repository_url: https://gitlab.momo86.net/mutsuki/nccl
    - repository_branch: master
    - shell_config: .bashrc
```
1. Run `ansible-playbook`
```
$ ansible-playbook -i hosts playbooks/mynccl.yml
```
