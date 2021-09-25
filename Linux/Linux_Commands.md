Linux Commands

Connecting to the Jump Box via SSH

```bash
ssh <username>@<Jump Box Public IP>
```
Once an SSH connection is established the Ansible Provisioner needs to be started

```bash
sudo docker start <container name> 
```
After starting our container we can verify its running by 

```bash
sudo docker ps
```
Attaching to the Docker container is the next ste

```bash
sudo docker attach <container name>
```

Once the playbook has been downloaded using ```curl``` the Ansible playbook can be run with the following command
from our Ansible node.

```bash
ansidle-playbook install-elk.yml
```

To check if our 