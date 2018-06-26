tomcat_pablo
=========

Deploys a Tomcat server running the application THREDDS, after installin Java, which is required for the application.


Requirements
------------
No requirements.

Role Variables
--------------
All variables in this role are defined in `defaults/main.yml`.

* java_directory -> Directory where Java will be installed on the remote server.
* jdk_version -> This variable stands for the final folder where all Java files will be, and has the name of the version of the Java Development Kit (ex:jdk1.8.0_171)
* tomcat_directory -> Directory where Tomcat will be installed on the remote server.
* tomcat_version -> This variable stands for the final folder where all Tomcat files will be, and has the name of the installed version (ex:apache-tomcat-8.5.31)  
Dependencies
------------
No dependencies  
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: True
      roles:
         - role: tomcat_pablo
Important notes
-------
* In order to run the `startup.sh` script correctly the `nohup` command must be added to ignore the HUP (*hang up*) signal. The built-in Tomcat management scripts like `startup.sh` don't detach from the tty, so the process would be killed when Ansible is finished.

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
