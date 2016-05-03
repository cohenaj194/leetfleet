leetfleet creates fleet service files for web facing application containers
It creates the following:
  - a service to deploy a web application container (someapp@.service),
  - a discovery service file for those containers (someapp-discovery@.service,  
  - and a load balancer that uses the discovery service load balancing the containers (someapp-lb@.service)
  - a new directory in the cloned repositories temp/ directory that will store your new files

HOW TO USE:
1) in the leetfleet directory run the command
ansible-playbook leetfleet.yml

2) the playbook will prompt you to enter in info about your container and your desired name for your service

3) Your files will be in a direcory in the temp/ directory of leetfleet named after your service name.  For example if you named your service AA, your files would be in the directory leetfleet/temp/AA/