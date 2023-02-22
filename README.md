# Easy Dynamics Ansible Configuration for Linux

Assists in configuring an Ubuntu-based machine (either native, a VM, or WSL) with various software
for projects at Easy Dynamics. 

## Prerequisites

Both `git` and `ansible` are necessary in order to run the playbook. Install both tools using
`apt`:

```
sudo apt update && sudo apt install git ansible
```

## Running

Run playbook with:

```
PYTHONUNBUFFERED=1 ansible-pull -U https://github.com/EasyDynamics/linux-dev-setup --directory "$(mktemp -d)" --purge -i hosts -K setup.yml
```

When prompted for the `BECOME` password, enter the password for your user within WSL.
