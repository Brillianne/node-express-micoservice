In the same directory checkout into a branch named "Stage_two". Create a new directory in the stage-1-Ansible-root folder and name it after the branch you just checked into

Create a Vagrantfile, copy the following file

Vagrant.configure("2") do |config|

config.vm.box = "geerlingguy/ubuntu2004"

end

and run command vagrant up

# Ansible Role
In your directory, run the command #ansible-galaxy init (name of the role) to create an ansible role

Navigate to tasks directory. In the main.yml define the tasks to clone the repository,pull both backend and client images, copy docker-compose.yml file to a folder and run the compose file to start the containers.

# Terraform for Infrastructure provision
On stage_two directory , create main.tf file  then define the infrastructure to be provisioned

Create a playbook.yml file to Defineplays to provision infrastructure using terraform and run the containers from the docker-playbook.yml file.

Confirm the services are running and accessible by running below command and making sure all the steps/tasks are being run successfully.

` ansible-playbook docker-playbook.yml 
