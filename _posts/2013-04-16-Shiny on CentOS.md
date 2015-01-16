---
published: true
title: Installing R shiny On CentOS server
layout: post
tags: [Unix, R]
modified: 2013-04-16 
image: 
comment: true
---

In the last four months I had worked to develop a web application with shiny server to analyze with Kernel density estimation  the density of TV viewers in Tunisia. I will write an installation guide that will help you if you need to use CentOS 32 bits or 64 bits.


I’m a root user :) !

Through my experience , I can advise you to install these development libraries first


         yum install libssl-dev
         yum install openssl-devel

Install Node.js from the official web site See related article here
      cd /opt
      wget http://nodejs.org/dist/latest/node-v0.10.5.tar.gz
      tar -xvf node-v0.10.5.tar.gz
      cd node-v0.10.5
      ./configure && make && sudo make install


Now, you can install R  but before, this  you make sure to install epel repos  

      wget http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
      sudo rpm -Uvh remi-release-6*.rpm epel-release-6*.rpm
      ls -1 /etc/yum.repos.d/epel* /etc/yum.repos.d/remi.repo
      /etc/yum.repos.d/epel.repo
      /etc/yum.repos.d/epel-testing.repo
      /etc/yum.repos.d/remi.repo

with this command vi /etc/yum.repos.d/ you can see all installed repos,   and change enabled from 1 to 0
Then you are ready to install R and Rstudio server If you want ;)

    yum install -y R-base 
    cd /tmp/
    wget http://download2.rstudio.org/rstudio-server-0.97
    .449-x86_64.rpm
    yum install --nogpgcheck rstudio-server-0.97.449-x86_64.rpm

to Install npm 

         yum install npm

 Install Shiny server with npm command 

        npm install -g shiny-server

After finishing the installation you can configure ;

         cp –R config/upstart/shiny-server.conf /etc/init/

you can start shiny server now !

          start shiny-server
          
Finally, I installed packages using the terminal not R studio server because it simplify for me the UNIX File Permissions  but you can change it with the chmod command.

         su - -c "R -e \"install.packages('dbconnect',repos='http://cran.r-project.org/')\""


That's it ! please let me know if it was helpful for you  .

