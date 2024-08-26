An `Ansible` playbook that allows you to deploy Docker containers for:
* Apache2
* MySQL

#Structure
The playbook itself has only one task which reads the control variables and enables the roles to perform the tasks required by the users.
```
.
├── ansible.cfg
├── defaults
│   └── main
│       ├── crlxc.yml
│       ├── crusers.yml
│       ├── plbook.yml
│       ├── ublamp.yml
│       └── ubupdate.yml
├── inventory
├── README.md
├── roles
│   ├── create_containers
│   │   ├── files
│   │   │   ├── apache2
│   │   │   │   ├── html
│   │   │   │   │   └── pablosdungeon.com
│   │   │   │   │       └── index.html
│   │   │   │   ├── sites-available
│   │   │   │   │   └── pablosdungeon.conf
│   │   │   │   └── ssl
│   │   │   │       ├── certs
│   │   │   │       │   └── localhost.crt
│   │   │   │       └── private
│   │   │   │           └── localhost.key
│   │   │   └── mysql
│   │   │       └── db1
│   │   ├── tasks
│   │   │   ├── apache2_lxc.yml
│   │   │   ├── install_azcli.yml
│   │   │   ├── install_azcopy.yml
│   │   │   ├── install_docker.yml
│   │   │   ├── main.yml
│   │   │   ├── mkbackup.yml
│   │   │   └── mysql_lxc.yml
│   │   └── templates
│   │       ├── dockerfiles
│   │       │   └── apache2
│   │       │       └── Dockerfile
│   │       └── make_backup
│   ├── create_users
│   │   └── tasks
│   │       ├── add_sudoers.yml
│   │       ├── main.yml
│   │       └── ssh_copy.yml
│   └── ubuntu_update
│       └── tasks
│           └── main.yml
├── site.yml
└── tasks
    └── main.yml
```
23 directories, 27 files
