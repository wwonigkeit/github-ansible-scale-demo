# github-ansible-scale-demo
The repository is used as a demo platform for GitHub, Ansible, AWS, GCP an Vorteil integration

# What are we trying to achieve
In a couple of simple steps:

1. Edit the "/usr/share/nginx/html/index.html" file within the repository and commit the change
2. GitHub actions will offload a pull and build request to Ansible (or Ansible Tower)
3. Ansible (Tower) will pull the repository and build a new Vorteil machine using the configuration file
4. Ansible (Tower) will provision the image (or ask Vorteil to do it) to AWS and GCP
5. Ansible (Tower) will create the machine (or replace) the machine if it currently exists

Things to consider:

1. Do we create the load-balancer as well - what if it exists?
2. Do we upate the DNS as well with the new pointer?
