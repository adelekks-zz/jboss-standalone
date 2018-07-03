## Standalone JBoss Deployment

- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6 or 7 hosts

These playbooks deploy a very basic implementation of JBoss Application Server,
version 7. To use them, first edit the "inventory" inventory file to contain the
hostnames of the machines on which you want JBoss deployed, and edit the 
group_vars/all file to set any JBoss configuration parameters you need.

Then run the playbook, like this:

	./jboss.yml

When the playbook run completes, you should be able to see the JBoss
Application Server running on the ports you chose, on the target machines.

This is a very simple playbook and could serve as a starting point for more
complex JBoss-based projects. 

## Application deployment

The playbook deploy-application.yml may be used to deploy the HelloWorld JBoss hosts that have been deployed using site.yml, as above.

Run the playbook using:

	./jboss-deploy-app.yml
	
The HelloWorld application will be available at `http://<jboss server>:<http_port>/helloworld`
