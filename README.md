![flow diagram](https://raw.githubusercontent.com/redx1t/aws-training-udacity-project-2/master/images_on_deployment_process/Udacity%20Infrastructure%20as%20Code%20Image.png)

# HOW TO DEPLOY

clone this repository and navigate to the file root

configure aws cli

create key pairs to use and change it in the script on the {KeyName} section on the WebAppLaunchConfig

test the config then run the below commands to

1. setup the network

./create.sh UdagramAppNetwork network.yml network_parameters.json

2. setup the server

wait for the network to create succesfully

./create.sh UdagramAppServer server.yml server_parameters.json

view the loadbalancer url as output from the UdagramAppServer stack

# FILES EXPLANATION

network.yml and network_parameters.json represent template-body and parameters consecutively for the network setup

server.yml and server_parameters.json represent template-body and parameters consecutively for the server setup

create.sh, update.sh and destroy.sh are bash files for executing create, update, destroy on stacks
