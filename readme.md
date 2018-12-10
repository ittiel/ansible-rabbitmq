  
# Ansible - rabbitMQ installation example

Example for Ansible installing rabbitMQ on hosts 
For the demo simplicity - using localhost

## Including:

 - Adding a queue HA_tasks
 - All queues that match the pattern HA_* should be highly available
 - Create an admin user with all permissions
 - Create monitor user that can read the cluster status
 - Create tasks_read user that can read from HA_tasks queue
 - Create tasks_write user that can write to HA_tasks queue

## Not including:

- Ports configuration


## Running example:
Set the ansible configuration: 
`export ANSIBLE_CONFIG=ansible.cfg`

Run the playbook (verbose):
`ansible-playbook rabbitmq.yml -vvv`

## Todo:

 - Passwords are currently part of the vars, but should be extracted to vault
- Use ansible folder template
- Extract tasks from current rabbitmq.yml file
