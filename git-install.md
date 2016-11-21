Install and Config

This section covers the git program installation and configuration.

 

Installation

 

John¡¦s team has development machines running Windows and Mac. The servers are running Linux. To begin with git version control, the team install the git program in these operating systems.

 

In Windows, they use the installer because it handles everything we need to run git on Windows. It also include a GUI helper. In Mac, the git comes with Xcode¡XA development IDE for Mac. In some Mac that don¡¦t have Xcode installed, they install the git program with the brew.

 

In their Linux server, the team uses the build in package manager, e.g. apt-get for Ubuntu, to install the git program. 

 

Now, assuming we are part of John¡¦s team. We are going through the class to learn git version control to fit our development team¡¦s code versioning requirement.

 

Configuration

 

After installed the git program, we need to config it. At least, we need to set the username and email address so that we can know who is making changes on the code.

 

In command prompt, run the following command.

 

NOTE: This is my information, you may want to set yours.

 

Set up user name and email:

 
git config --global user.name "Thomas Seng Hin Mak"
git config --global user.email "mak@makzan.net"


 

This is the information that we can trace who has been working on what later when we need to collaborate the code with other members in the team.

 

NOTE: You can set project specific name and email by running the git config command without the --global option.

 

# cm461-11-2016-c
