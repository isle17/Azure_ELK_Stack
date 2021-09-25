Linux Commands

Connecting to the Jump Box via SSH:

```bash
ssh <username>@<Jump Box Public IP>
```
Once an SSH connection is established the Ansible Provisioner needs to be started:

```bash
sudo docker start <container name> 
```
After starting our container we can verify its running by:

```bash
sudo docker ps
```
Attaching to the Docker container is the next step:

```bash
sudo docker attach <container name>
```

Inside the container download the ```intall-elk.yml``` from the repository by:

```bash
$ curl https://raw.githubusercontent.com/isle17/Azure_ELK_Stack/main/Ansible/install-elk.yml >> install-elk.yml
```

Make sure that this file is downloaded the ```/etc/ansible``` directory 



Once the playbook has been downloaded the Ansible playbook can be run with the following command from our Ansible node.

```bash
ansidle-playbook install-elk.yml
```

To check if the install was successful: 

```bash
ssh <username>@<ELK-VM Private IP Address>
```

 and then use ```docker ps``` to see if the ELK instance is running