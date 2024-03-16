# Software-network
# Summary
## The code is an Ansible playbook (docker_deploy.yml) designed to automate the deployment of Docker containers, specifically an Apache web server container, on various #Linux distributions. The playbook is structured to ensure compatibility with both Debian-based (e.g., Ubuntu) and RedHat-based (e.g., CentOS) systems.
# Key Components:
## 1.Installation of Docker: The playbook begins by installing Docker on the target machines. It installs necessary system packages, adds Docker's official GPG key and #APT repository for Debian-based systems, and sets up the Docker repository for CentOS systems.
## 2.Deployment of Apache Docker Container: Following the Docker installation, the playbook proceeds to deploy an Apache Docker container. It pulls the Apache Docker #image, runs the container, and exposes port 80 to enable access to the Apache service.
## 3.Networking Configuration: The playbook configures networking for the Apache Docker container, assigning it to the apache_network network with a specified subnet ###(172.168.10.0/30). This ensures proper network communication and accessibility from the host machine.
## 4.Conclusions: After deploying the container, the playbook verifies connectivity to the Apache service by checking accessibility on port 80. It waits for a specified #timeout period to ensure a successful connection.
