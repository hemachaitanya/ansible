###  What is Ansible? 

* Ansible is one of the configuration Management Tools. It is a method through we automate system admin tasks. 

* Configuration refers to each and every minute details of a system. If we do any changes in system means we are changing the configuration of a machine.
* That means we are changing the configuration of the machine.

* All windows/Linux system administrators manage the configuration of a machine manually. 
* All DevOps engineers are managing this configuration automatic way by using 
some tools which are available in the market.

* One such tool is Ansible. That’s why we call Ansible as 
configuration management tool

## ansible 

* ansible is a configuration management tool & default pip3 also installed with ansible

* master: ansible , 

* nodes: agent ,

###  Working process of Ansible? 

* Here  we  crate  file  called  playbook  and  inside  playbook  we  write  script  in  YAML  format  to  create 
infrastructure.

* Once we execute this playbook, automatically code will be converted into 
Infrastructure.  
* We  call  this  process  as  IAC  (Infrastructure  as  Code).

* We  have  open  source  and enterprise editions of Ansible. Enterprise edition we call Ansible Tower.

### The architecture of Ansible? 

* #### Server: – 
It is the place where we create playbooks and write code in YML format 

* #### Node: – 
It is the place where we apply code to create infrastructure. Server pushes code to nodes.

* #### Ssh: – 
It is an agent through ansible server pushes code to nodes.  

* #### Setup: – 
It is a module in ansible which gathers nodes information.  

* #### Inventory file:-
 In this file we keep IP/DNS of nodes. 
 ###  Advantages of Ansible over other SCM (Source Code Management) tools?  
• Agentless  
• Relies on “ssh”  
• Uses python  
• Push mechanism 

### What do you mean by Ad-Hoc commands in Ansible?

* These are simple one liner Linux commands we use to meet temporary requirements without actually saving for later. Here we don’t use ansible modules.
 * So there, Idempotency will not work with Ad-Hoc commands.
* If at all we don’t get required YAML module to write to create infrastructure, then we go for it.
* Without using playbooks, we can use these Ad-Hoc commands for temporary purpose.  

###  Differences between Chef and Ansible?  
• Ansible - chef  
• Playbook – Recipe  ( play means collection of tasks )
• Module – Resource  ( )
• Host – Node  
• Setup – Ohai  ( maintaines the node information)
• Ssh – Knife  
• Push-Pull

###  Mention some list of sections that we mention in Playbook?  

  #### 1. Target section
  * In this section, we mention the group name which contains either IP addresses or Hostnames of nodes.
    * When we execute playbook, then code will be pushed too all nodes which are there in the group that we mention in Target section.
    * We use “all” key word to refer all groups.

 #### 2. Task section 
 * All tasks we mention in this task section. We can mention any no of 
modules in one playbook. 
* There is no limit. 
* If there is only one task, then instead of going with big playbook, simply we can go with arbitrary command where we can use one module at a time.
 * If more than one module, then there is no option except going with big playbook.

#### 3. Variable section
  We have this concept in each and every programming language and scripting language. We use “vars” key word to use variables.  
#### 4. Handler section

Sometimes you want a task to run only when a change is made on a machine.
  

### configuration management
* In configuration management is to automate the admin tasks what we do manually

* We can increase uptime so that can provide maximum user satisfaction.

* Improve the performance of the system
* Ensure compliences
* prevent errors as tools won't any error
* Reduce cost
#### configuration management are devided into two types

Direction of Communication

PULL => Node to CM server
    * Chef
    #### chef:
    (1)  Managed/Hosted  chef.
    (2)  Graphical user interface , it's not free
    (3) We can launch one server and we need to install chef server package. It is completely free 
package. It’s CLI (Command Line Interface).
    * Puppet
Push => CM Server to Node
List of nodes (inventory)
    * Ansible
    * SaltStack


* (1) push based configuration management
* (2) pull based configuration management

###  What is Idempotency? 

#### idempotence: 
Run this once or n times you will have same result

* It won’t do the same task again and again.
* If any new changes are there in that code, then only chef-client is going to take action. 
* So it doesn’t make any difference ever if you run chef-client any no of times. 
* So tracking the system details to not to reapply changes again 
and again, we call Idempotency

#### Desired state: 
We express configuration to acheive a desired state.

### configuration drift:
    * difference between desired state and actual state 

### * Why are we using loops concept in Ansible?  

* Sometimes  we  might  need  to  deal  with  multiple  tasks. 
* For  instance,  Installing  multiple  packages, Creating  many  users,  creation  many  groups. 
   Etc.  In  this  case,  mentioning  module  for  every  task  is 
complex process.
 * So, to address this issue, we have a concept of loops.
  * We have to use variables in combination with loops.

###   
