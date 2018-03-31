# fp-jenckins
Install Jenkins master
Step one:
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
Step two: After installation save the temporary password to activate Jenkins initially. It can be also retrieved from here:
/var/lib/jenkins/secrets/initialAdminPassword
Navigate to "http://<your instance/vm ip>:8080" and initiate the Jenkins master.

Step three: Select "Suggested Plugins" installation type.

Step four: Create yourself an admin account.

Configure a single SSH slave for Jenkins
Step one:
Navigate to "Manage Jenkins"
"Manage Plugins"
"Install SSH Agent Plugins"
After reload, go to "Credentials" and select all providers and types.
"Manage Nodes"
Add an SSH Node
Fill out Credentials Further examples for setup: https://wiki.jenkins.io/display/JENKINS/SSH+Slaves+plugin
Install Java on slave if needed. https://www.digitalocean.com/community/tutorials/how-to-install-java-on-ubuntu-with-apt-get
Voila!

#For running the tests
