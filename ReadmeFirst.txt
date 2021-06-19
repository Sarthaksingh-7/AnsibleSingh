1 Changing user to root user:

Sudo su

2 lets download epel package i.e extra package for enterprise linux.

wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm

3 you can check if the package is visible or not by "ls" command.

4 yum install epel-release-latest-7.no arch.rpm // installs the downloaded epel package.... type yes , yes to complete. 

5 try updating   
  yum update -y
6 Now install your required packages: 
yum install git python python-level python-pip openssl ansible -y

7 check if ansible is installed or not

ansible --version

8 Go to ansible hosts file
 vi /etc/ansible/hosts  // VIM editor will open for your hosts file in the inventory

9 Press I to Insert.

Lets create a group named 

[ubuntu server group]
private IP of the node ubuntu server.
 
you can also add your other nodes by adding any private IP or groups.

10 Go to ansible confg file.
  
   vi /etc/ansible/ansible.cfg 
11 Press I and go to input mode.

Activate inventory by removing the cooment:  

#inventory ----->  inventory
#sudo_user ----->  sudo_user

press :wq save an quit

12 Lets create an ansible user.

adduser ansibleusername
passwd ansibleusername // password for ansibleuser 

Change the password // user sucessfully added.


we can create the same user in node server also.


13 now change user to ansibleuser 

su - ansibleuser1

14  Give ansibleusr1 suoers right . 

exit  // exit and go to root again.
visudo  // a file will open.

go to " ALL root to run any command anywhere" and type.

root ALL=(ALL)
ansibleusr ALL=(ALL) NOPASSWD: ALL

:wq and exit 

do the above same on all nodes.

sudo yum install httpd -y

15 Try ssh into node machine from ansible server // it will not be done as the access has not been given to ansibleuser to do that.
 vi /etc/ssh/sshd/sshd_config

need to have three important changes here.
uncomment Pertmitlogin
Uncomment PasswordAuthentication yes
comment PasswordAuthentication no

16 restart sshd service

service sshd restart

17 Change to ansible user

su - ansibleusr1 //and try ssh to node server IP
ssh privateip

18 Now creata a key in ansible server and copy the pub key into node server so that it does not ask password again.
create trust relationship.
user to user....  // here use anibleuser as an ansibleuser

19 in ansibleserver:  
ssh-keygen // private public key will be created

cd . ssh/
ls -a /// -a because it is a hidden file... id-rsa is private key .... id_rsa.pub is a public key

20 Copy the public key to node.
ssh-copy-id ansibleusr1@nodeprivateip


21 Now creating Ansible Playbook.
everthying is to be done by ansibleur1

ls

rm -rf *

ls

22 now create a yml file.
vi playbookfile.yml

23 run yml playbook
ansible-playbook playbookfile.yml






 
