# Configure NTP and Apache using Ansible

## Description ## 
- USing Ansible we could configure client machines, by running those configurations in the master node

- Here, we have 2 Roles [Apache role and NTP role], each role is on github Repo
- each Role-Repo is mentioned in file **roles/requirements.yml** 
   - **Apache Role:** [Github_Repo_link](https://github.com/salma-ahmed20/Apache-Role-Ansible.git)
      - install httpd service, enable and start it
      - copy from master node **index.html** file to  client in Path **/var/www/html/index.html**
      - allow port 80 on firewall and reload firewalld
   - **NTP Role:** [Github_Repo_link](https://github.com/salma-ahmed20/NTP-Role-Ansible.git)
     - ensure that chrony is exist 
     - copy from master node **chrony.conf** file to  client in Path **/etc/chrony.conf**
     - enable and start chronyd service
