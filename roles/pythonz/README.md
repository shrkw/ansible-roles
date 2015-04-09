Pythons Ansible Role
===============================

* Set up development dependencies for Python compiling (CentOS and Ubuntu convertible)
* Install Python binary (default: 2.7.8)
  * You can modify `vars`, if you want to install other binaries
* Install pip to system default Python
* Install virtualenv

After running this role, you can install your dedicated Python environment by following commands.

```
virtualenv -p /usr/local/pythonz/pythons/CPython-2.7.8/bin/python ~/.virtualenvs/CP278
source ~/.virtualenvs/CP278/bin/activate
```

Shortcut Usage
---------------------------

I stored default `playbook.yml` file for convenience.
If you want to run just this role, you can just create `hosts` file,

```hosts
[target]
127.0.0.1 ansible_ssh_port=2200 ansible_ssh_user=vagrant ansible_ssh_private_key_file=/Users/shrkw/.vagrant.d/insecure_private_key
```

You can execute as a simple playbook.

```
ansible-playbook -i hosts site.yml
```
