# Ansible Playbooks for my Raspberry Pis

* Install requirements from Ansible Galaxy:  
`sudo ansible-galaxy install -r requirements.yml`
* Run base playbook (as user `pi`):  
`ansible-playbook base.yml -i hosts`
* Run other playbooks (as user `thomas`):  
e.g.: `ansible-playbook ozwcp.yml -i hosts`

## Playbooks

### Base (base.yml)

* Runs a full apt package upgrade/update
* Extends the root filesystem to the actual SD Card size
* Configures time zone, locale