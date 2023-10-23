# My E-commerce Application Deployment with Ansible

Follow these steps to set up and deploy the containerized E-commerce application on your computer using Ansible.

## Prerequisites

Ensure you have the following prerequisites installed on your computer:
- [Vagrant]
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Python 3](https://www.python.org/downloads/)

## Getting Started

1. **Clone the Repository**

  
   git clone https://github.com/WanguiR/yolo_ansible/
   cd YourRepository

2. **Create an Ansible Playbook**

Created an Ansible playbook [playbook.yml] in the project directory and defined the tasks for setting up the application.
Tasks included:
- installing packages
- cloning the application code
- copying docker-compose file
- setting up front end and backend of the application 

3. **Define Your Ansible Roles**

Organized my Ansible roles for the frontend and backend components. Ensured that each role has a structured directory with a tasks/main.yml file.
Roles 
`client` - conatining a tasks/main.yml file that copies the dockerfile from application code and builds and start the frontend container
`backend` - conatining a tasks/main.yml file that copies the dockerfile from application code and builds backend container


4. **Update Variables and Paths**

Review the playbook and roles to ensure that variables and paths match your specific project requirements. Customize the variables to suit your needs.

5. **Deploy the Application**
Run the Ansible Playbook inside the path yolo_ansible/ansible

Executed the Ansible playbook to set up and deploy the application with this command

 ansible-playbook playbook.yml

This command configured the server, cloned the application code, set up the frontend and backend containers, and deployed the application.

6. **Access Your Application**

Once the playbook execution was complete, I could access the E-commerce application through a web browse by opening a browser and navigating to the server's IP address

Server IP: http://YourServerIP (here use the server ip of your server-couldnt write mine since its not best practice....)

Congratulations! Your E-commerce application is now up and running.

## Notes
Make sure your server's network settings allow incoming traffic on the necessary ports.
Ensure that you have the necessary permissions to execute the Ansible playbook and make system changes.


