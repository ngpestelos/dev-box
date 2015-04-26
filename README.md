dev-box
=======

Development toolbox.

* Ruby
* Go
* Docker

### Requirements

* Ansible 1.7
* a fresh server

### Usage

#### Customize `hosts`:

    $ cp hosts.example hosts

Replace `1.2.3.4` with your server's IP address.

#### Customize `authorized_keys`:

Replace with your public key.

#### Bootstrap the server

Do this at most once:

    $ ansible-playbook -i hosts bootstrap.yml -vvvv

Bootstrapping creates a `deploy` user and disables root login.

#### Continue with setup:

    $ ansible-playbook -i hosts site.yml -vvvv

#### Shell into the machine:

    $ mosh deploy@1.2.3.4

### License

MIT License.