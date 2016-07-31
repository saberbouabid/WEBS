---
published: true
title: Java installation on CentOS 6
layout: post
tags: [Unix, R]
modified: 2013-03-16 
image: http://www.javaassignmenthelp.net/wp-content/uploads/2013/06/Java-Assignment-Help.jpg
comment: true
read-time: false
---

Java today makes programs works perfectly like magic, but that not always the situation. My adventure with the famous framework dedicated to business intelligence Spagobi 3.6 server, Started with a problem of java compatibility, the server was working
in Centos 6 64 bits and it takes from me a lot of time to know what the problem and searching for the best solution important to choose the right package and the right version of Sun java...
I’m Sure that you hired by the OpenJDK  the java version delivered  by most the distributions of Linux ... Sometimes it works without any problem but for me nothing happens and ouups i come back to Google !!
Then I find the solution!! It works perfectly and I managed all java versions like  games. So if you have a problem with java try to understand haw I did it?!

What will we need:

 - The right Oracle JDK RPM version (from Oracle.com)
 - JPackage Utils
 - The Sun Compatibility package


We can get JPackage Utils by login in the terminal as root and write:
yum install jpackage-utils
Next step to download the Oracle JDK Linux RPM rpm.bin http://www.oracle.com/technetwork/java/javase/downloads
Or write this command:

    cd /tmp/
    wget http://download.oracle.com/otn/java/jdk/6u41-b02/jdk-6u41-linux-x64-rpm.bin
  
Now, to install it you will need to change his rights with chmod command.

    chmod 755 jdk-6u41-linux-x64-rpm.bin
    
To install it:

    ./jdk-6u41-linux-x64-rpm.bin
  
Right now you must have JDK and JRE 6 installed on your machine. But still a little thing  most important, you must know that every time you have to install a software depend to java yum will try to install Openjdk and that is a problem in my situation .the solution is the compact package  suitable to the java version which you have installed.
You can find the right one in the web site scientificlinux.org … I found it here 
http://ftp.scientificlinux.org/linux/scientific/5rolling/testing/x86_64/

The last step is to install it .

    yum localinstall ftp://ftp.scientificlinux.org/linux/scientific/5rolling/testing/x86_64/java/java-1.6.0-sun-compat-1.6.0.37-3.sl5.jpp.x86_64.rpm

Finally you must use the alternatives command to make Oracle JDK as your default one java package! Then when you installed tomcat for example it will accept this configuration directly...
And choose the number of java version which you want to use!

    alternatives  --config java
    java  -version
    javac  -version

And that’s the story of Java compatibility and Linux distributions

If you have any amelioration please let me know!
