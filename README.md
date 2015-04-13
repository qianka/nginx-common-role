nginx-common
============


Requirements
------------

- Ubuntu Server 14.04 LTS
- Ansible 1.5+


Role Variables
--------------

```yml
nginx_user: www-data;
nginx_worker: 8;
nginx_rlimit_nofile: 200000;

nginx_worker_connections: 65535
nginx_keepalive_timout: 60

nginx_access_log_options: ''
```


Dependencies
------------

- qianka.ubuntu-common


Example Playbook
----------------

```yml
- hosts: all
  user: root
  vars:
    ubuntu_apt_mirror: http://mirrors.aliyun.com/ubuntu

  roles:
    - { role: qianka.nginx-common,
        nginx_access_log_options: 'buffer=1024k flush=5m'
      }

```


License
-------


Author Information
------------------
