# phabricator-ansible

Ansible playbooks for Phabricator installations with Vagrant (optional).

**Before running this playbook on a production server, make sure that non of this configuration
break things or conflicts with your server**

## RHEL6

#### Installing

There is a Vagrantfile in the root of this repository in case you want to set it up
quick, just do `vagrant up` and you will have an instance up and running on http://phabricator.local

Add an entry to your host machine `/etc/hosts` file to this domain and that's it.

If you used vagrant before you should know the consequences of running a vagrant box in production.

In case you want to run just the ansible playbooks on a server:

`ansible-playbook -i rhel6/hosts rhel6/site.yml`


# LICENSE

```
Copyright (C) 2013 Juan Carlos Alonso

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
