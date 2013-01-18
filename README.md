# phabricator-ansible

Ansible playbooks for Phabricator installations.

**This is still in very active development, and might break...**

**NOTE: As of right now, this assumes that it's run on a dedicated
box that is ONLY RUNNING PHABRICATOR.**

**DO NOT RUN THIS BLINDLY ON A PRODUCTION BOX, IT _WILL_ BREAK THINGS**

## RHEL6

#### Installing

`ansible-playbook rhel6/phabricator.yaml --tags install`

Answer any prompts (currently just the domain on which Phabricator lives).

#### Upgrading

`ansible-playbook rhel6/phabricator.yaml --tags update`

Press enter, because the prompt doesn't matter for updates.

# LICENSE

```
Copyright (C) 2013 Ricky Elrod

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
