# Super Simple config loader tool

I needed a way to load a config from a system that could only talk
ansible, so this was born.

## Running


### Install / Upgrade the panos enhanced collection

`ansible-galaxy collection install --force mrichardson03.panos`

### Create / edit  your inventory file

`cp inventory.sample inventory`

`vi inventory`


### Run the Playbook, passing along extra vars if necessary

`ansible-playbook -i inventory load_config.yml -e 'ansible_host=10.10.10.2' -e 'ansible_user=player1' -e 'ansible_password=entered_the_chat!' -e 'fw_config=Default.xml'`
