## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

https://github.com/sguarino21/Azure-Peered-Networks.git

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the https://github.com/sguarino21/Azure-Peered-Networks.git repository may be used to install only certain pieces of it, such as Filebeat.

  - List of All Configuration and Playbook files to recreate environment:
  
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/ansible_config.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/filebeat-config.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/filebeat-playbook.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/hosts_yml.yaml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/install-elk.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/metricbeat-config.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/metricbeat-playbook.yml
  - https://github.com/sguarino21/Azure-Peered-Networks/blob/main/pentest.yml


  - https://github.com/sguarino21/Azure-Peered-Networks.git


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to filtering access to the network.
- Load balancing is effective at preventing DDoS attacks. The advantage of the JumpBox is essentially to provide a gateway router to your private network ensuring that all of your other machines in the network do not directly face the internet providing a more secure network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the network and system logs.
- Filebeat collects data about the file system, including which files have changed and when they were changed.
- Metricbeat collects machine metrics, such as uptime.

The configuration details of each machine may be found below.


| Name     | Function |-------------| IP Address | Operating System |
|----------|----------|-------------|-------------------------------|
| Jump Box | Gateway Router         | 10.0.0.1   | Linux   |
| Web-1    | DVWA Container         | 10.0.0.7   | Linux   |
| Web-2    | DVWA Container         | 10.0.0.8   | Linux   |
| Web-3    | DVWA Container         | 10.0.0.9   | Linux   |
| ELK      | ELK Server             | 10.1.0.4   | Linux   |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the JumpBox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 73.99.142.164

Machines within the network can only be accessed by JumpBox.
- The ELK server may be accessed from the Web-1, Web-2, Web-3, and JumpBox machines.

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- The main advantage of automating configuration with Ansible is that it enables IT administrators the ability to automate your daily work tasks and give the administrator more time to focus on the needs of the business, thus providing more value to the company.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- Web-1 // 10.0.0.7
- Web-2 // 10.0.0.8
- Web-3 // 10.0.0.9


We have installed the following Beats on these machines:
- Filebeat
- Metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._