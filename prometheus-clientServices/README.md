prometheus-clientServices
=========================

Performs the prometheus and grafana deployment which supports the client services team.

ec2-install.yml is an example implementation of a playbook which provisions and deploys to arbitrary AWS based on tags.
To implement a similar playbook, you'll need to copy identify_aws_hosts.yml and bootstrap_aws_hosts.yml into your project,
add the appropriate group_vars and inv, then write a playbook to use it all. 

Requirements
------------

aws deploy requires python boto module: `pip install boto`
requires docker. 

Playbook Variables
------------------

bootstrap - true if ec2-install.yml should do a full bootstrap of the VMs (required for new VMs) 
    or if it should just update existing grafana and prometheus installations.

Example Execution
-----------------

ansible-playbook -i inv/merlin-compass-us-east/merlin-compass-us-east ec2-install.yml -e bootstrap=true

Author Information
------------------

Chennai
