For avoiding problem with linux permissions in Windows 10, you should create virtual volumes for each block

Use the commands 
docker volume create data-gitlab
docker volume create logs-gitlab
docker volume create config-gitlab
docker volume create data-jenkins

For handling with terminal in each container you should use the command
docker exec --it {container-id} /bin/bash

For avoiding comunication problems between jenkins and gitlab, you should use reference their ips when
they need this communitation, for example  git@172.22.0.2 is the ssh route for the gitlab server (172.22.0.2)