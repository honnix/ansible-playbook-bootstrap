# ansible-playbooks-bootstrap
The playbooks to bootstrap playbooks

## Run

```
$ git clone https://github.com/honnix/ansible-playbooks-bootstrap.git
$ cd ansible-playbooks-bootstrap
$ ansible-playbook -i inventory site.yml
```

This will create a directory named `playbooks` in the same directory
where the repository sits. For example if the repository is
`~/ansible-playbooks-bootstrap`, then `~/playbooks` will be created.
However if this is not what you want, run this instead:

```
$ ansible-playbook -i inventory site.yml -e "where=[path]"
```

`path` denotes where the top level directory should be.

By default empty directories will be filled in with `.gitignore`, but
if this is not wanted, run this:

```
$ ansible-playbook -i inventory site.yml -e "fill_in_empty=false"
```
