Exp 1 : Create a Repository

AIM:
To create a repository.

EQUIPMENT REQUIRED:
Hardware: Minimum 4 GB RAM and 25 GB storage – essential for running services like Cockpit and handling system updates smoothly.
Software: Red Hat Enterprise Linux (RHEL) or any open-source Linux OS like Fedora or CentOS Stream – used for system administration and repository creation.

PROCEDURE & COMMENTS:
SSH login
The first line shows an SSH login to a server with the IP address 172.25.250.11. The user logging in is root . SSH (Secure Shell) is a network protocol that allows secure remote login to a server. The root user is the system administrator account and has full access to all commands and files on the system.
Enabling the web console
The next line shows a command to activate the web console with systemctl enable-now cockpit.socket. Cockpit is a web-based interface for managing Linux systems. Enabling the socket tells the system to start the Cockpit service whenever the system boots.
Registering with Red Hat Insights
The line insights-client-register registers the system with Red Hat Insights. Red Hat Insights is a subscription service that provides system health reports and recommendations for security and performance improvements.
Viewing Yum repositories
The user then edits the file /etc/yum.repos.d/local.repo using the vi text editor. Yum is a package manager for Red Hat-based systems. Repos (repositories) are locations where software packages are stored. The local.repo file likely contains configuration information for custom yum repositories.
Checking Yum repository information
After editing the file, the user uses the cat command to view the contents of /etc/yum.repos.d/ local.repo. The cat command is used to display the contents of a file.
Cleaning Yum packages
The next command is dnf clean all. Dnf is a newer version of yum that is used in Red Hat Enterprise Linux 8 and later. The clean all command removes cached package metadata.
Listing Yum repositories
The user then uses the dnf repolist all command to list all configured repositories. The output shows two repositories configured: appstream and baseos. These are the default repositories for Red Hat Enterprise Linux 9.
Installing Vim
The final command is dnf install vim -y. This command installs the Vim text editor using the dnf package manager. The -y flag tells dnf to assume yes to all prompts, which is useful for unattended installations.

OUTPUT:



![Exp 1](https://github.com/user-attachments/assets/f861940b-29db-448f-a2fd-33c36fa27458)


RESULT:
Thus a repository has been created successfully. 









