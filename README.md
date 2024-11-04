#  Web Service Deployment Project

## Project Overview

This project automates the deployment and configuration of a web service using Ansible. The project structure is modular, focusing on clarity and ease of customization. It deploys a secure, SSL-enabled web service with user authentication and custom port management.


## Project Structure

```web_service_deploy/
├── README.md
├── inventory
│   └── server_list
├── global_vars
│   └── main_config.yml
├── components
│   └── web_handler
│       ├── tasks
│       │   └── install_config.yml
│       ├── templates
│       │   ├── vhost_template.j2
│       │   └── access_control.j2
│       └── vars
│           └── settings.yml
└── deployment.yml
```


## How to Run the Project

-  -   Clone the repository and navigate to the project directory.
-   Ensure your Ansible control node has the necessary permissions and SSH access to the managed nodes.
-   Modify the `inventory/server_list` and configuration files as needed.
-   Run the playbook:    
    `ansible-playbook deployment.yml -i inventory/server_list`

## Variables and Prompts
The `deployment.yml` playbook prompts for the `input_hostname` at runtime. Ensure the hostname provided matches the server's configuration.
