ansible-backup_local-patch
===============

patch for custom backup (ansible/module_utils/basic.py).  
It provides workaround for the issue https://github.com/ansible/ansible/issues/16305  
after apllied this patch, ```backup``` directive will backup files in ```/var/log/ansible/backup/<date>/```

### usage

example for ubuntu:
```shell
git clone https://github.com/nohi/ansible-backup_local-patch.git
cp ansible-backup_local-patch/custom-backup.patch /usr/lib/python2.7/dist-packages/ansible/module_utils/
cd /usr/lib/python2.7/dist-packages/ansible/module_utils/
patch < custom-backup.patch
```

### file location

| OS           | location     |
|:------------:|:-------------|
| centos6(yum) | /usr/lib/python2.6/site-packages/ansible/module_utils/basic.py |
| ubuntu(apt)  | /usr/lib/python2.7/dist-packages/ansible/module_utils/basic.py |

### Operation check

| Ansible Version | work          |
|:---------------:|:-------------:|
| v2.2.0.0        | 〇            |
| v2.1.2.0        | 〇            |
| v2.1.1.0        | 〇            |
| v2.0.0.0        | 〇            |
