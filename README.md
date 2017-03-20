dev-box
=======

Ansible playbook to setup a development environment.

### Why

While Vagrant provides an isolated environment, but doesn't provide a way around slow Internet connections.

It is much faster to install dependencies inside a VPS.

A development box is intended to be a disposable environment.

### Requirements

* Ansible 1.7
* a fresh server

### Usage

#### Update `authorized_keys`:

Replace with your public key.

#### Create inventory file:

```
cp hosts.example hosts
```

Replace `1.2.3.4` with your server's IP address.

#### Run the playbook

```
ansible-playbook -i hosts site.yml -vvvv
```

#### Shell into the machine:

    $ mosh deploy@1.2.3.4

### License

MIT License.
