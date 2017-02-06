# Ansible Playbooks for my Raspberry Pis

* Install requirements from Ansible Galaxy:  
`sudo ansible-galaxy install -r requirements.yml`
* Check/set your preferred username in `vars/main.yml`
* First run only: Run base playbook as default user `pi`:  
`ansible-playbook base.yml -i hosts -u pi --ask-pass`
* Subsequent runs:  
`ansible-playbook main.yml -i hosts`
* Or run specific playbooks only:  
`ansible-playbook ozwcp.yml -i hosts`

## Playbooks

### Base (base.yml)

* Runs a full apt package upgrade/update
* Extends the root filesystem to the actual SD Card size
* Configures time zone, locale

### OZWCP (ozwcp.yml)

* Installs [OpenZWave Control Panel](https://github.com/OpenZWave/open-zwave-control-panel)

### Mosquitto (mosquitto.yml)

* Installs the [Mosquitto](http://mosquitto.org) MQTT broker

### Misc (misc.yml)

This playbook performs some basic configurations I prefer to have available on my Linux machines.

* Create an `ll` alias for `ls -alF`
* Install `htop`