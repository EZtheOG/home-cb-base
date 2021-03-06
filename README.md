A Base Cookbook
=============
This is the base cookbook for every node in your infrastructure. This will install every package, user, sudo access, denyhosts, etc. that everynode will be using. Also, there are recipes in here that create users and you can call them from other cookbooks by calling ```cb-base::users-dev``` e.g.

At this time - this cookbook is written for the AWS Centos Environment.

Requirements
------------
In terms of testing, the LWRPs are:

depends 'ntp'
depends 'sudo'
depends 'poise-python'
depends 'yum'
depends 'user'
depends 'logrotate'
depends 'omnibus'
depends 'chef-client'

### Will need to add Sensu client as well along with other collectors.

This cookbook is tested and is working on Amazon CentOS based architecture. 


Attributes
----------
Attributes are listed in each attr file.

Default has all the system logic (packages, python modules, directories, etc.).
DenyHosts is all attributes for DenyHosts conf files and setup.
DNS is for DNS that is segmented out for each region/vpc subnet.


Contributing
------------

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

All code is reviewed before pushed into Prod.

If you want to fork this as a springboard into your cookbook, please do! 

License and Authors
-------------------
Authors: EZ Bardeguez 
