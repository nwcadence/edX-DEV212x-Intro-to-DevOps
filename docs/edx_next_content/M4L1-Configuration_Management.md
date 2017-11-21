`Outline > Module 4: Configuration Management and Release Management > Configuration Management and Release Management > Configuration Management `

# Configuration Management #

### Configuration Management ###

- Configuration Management means the management of configuration of all environments for an application.
	- Typically in the form of scripts that are version controlled.
- Configuration Management in the DevOps world is less formal than "traditional" configuration management.
	- It emphasizes encapsulation of configuration in code over formal documentation.
	- It means lighter weight, executable configurations that allow us to have configuration and environments as code.
		- **Infrastructure as Code:** Defining your environments, to include networks, servers, and other compute resources as a text file (script or definition) that is checked into version control and is used as the base source for creating or updating those environments. For instance, adding a new server should be done by editing a text file and running the release pipeline, not by remoting into the environment and spinning one up manually.
		- **Configuration as Code:** Defining the configuration of your servers, code and other resources as a text file (script or definition) that is checked into version control and is used as the base source for creating or updating those configurations. For instance, adding a new port to a firewall should be done by editing a text file and running the release pipeline, not by remoting into the environment and spinning one up manually.

### Benefits of Configuration Management ###

Configuration Management provides the following benefits:

- Allowing configuration to be version controlled
- Detecting and correcting configuration drift
- Treating infrastructure as flexible resource
- Facilitating automation
- Enabling automated scale-up and scale-out
- Providing environment consistency

## Configuration Management ##
![](http://i.imgur.com/mBKU7Le.jpg)<br>
**[Video link: https://youtu.be/D4To34eL7eE]**


