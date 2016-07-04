localcloud-docker
=========

This role will install docker engine 1.11 on an Ubuntu 14.04 host, create proper groups and configure firewall as per official [install documentation](https://docs.docker.com/v1.11/engine/installation/linux/ubuntulinux/). 

Please note that it does not make any assumptions on how you will access docker socket, so it does not open up any ports. If you need external access you should open up desired ports either manually or using ansible [ufw module](http://docs.ansible.com/ansible/ufw_module.html) from your playbook.


Requirements
------------

This role tequires an Ubuntu 14.05 Trusty (LTS). It will probably work on newer releases as well.



Role Variables
--------------

`box_user`
The user that will be used to run docker. This user will be added to docker group and an additional tooling script will be installed.



Dependencies
------------

This role has no external dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - dmitrybelyakov.localcloud-docker

  vars:
    box_user: ubuntu

```

License
-------

The MIT License (MIT)
Copyright (c) 2016 Dmitry Belyakov

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


