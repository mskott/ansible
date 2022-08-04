# Server setup

Configures a freshly installed Fedora 35 Server

1. `ansible galaxy collection install -r requirements.yaml`
2. `ansible-playbook -i inventory.ini basics.yaml -K`
3. `ansible-playbook -i inventory.ini all-hosts.yaml`
