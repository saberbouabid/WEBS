---
published: true
title: How To Install Java on CentOS to use Spago BI 
layout: post
tags: [Unix, Java , CentOS]
modified: 2013-03-16 
image: 
    feature: java.jpg
comment: true
read-time: false
---



Java today makes programs works perfectly like magic, but this isn’t in my actual case.

My adventure with the famous framework dedicated to BUSINESS INTELLIGENCE Spagobi 3.6 server, Started with a problem of java compatibility. I spent a lot of time trying to know what is the issue and resolve it.
The best practice is to choose the right package and the right version of SUN java ... I discovered that _OpenJDK_ the java version delivered by most the distributions of Linux and by default CentOS use it instead of Sun Java required by Spago BI.


You will we need:

 - The right Oracle JDK RPM version (from [Oracle](www.oracle.com))
 - JPackage Utils
 - The Sun Compatibility package


We can get JPackage Utils by login in the terminal as root and write:

     yum install jpackage-utils
    
Next step ,you download the Oracle JDK Linux RPM _rpm.bin_ http://www.oracle.com/technetwork/java/javase/downloads
Or write this command:

    cd /tmp/
    wget http://download.oracle.com/otn/java/jdk/6u41-b02/jdk-6u41-linux-x64-rpm.bin
  
Now, to install it you will need to change its rights with _chmod_ command.

    chmod 755 jdk-6u41-linux-x64-rpm.bin
    
To install it:

    ./jdk-6u41-linux-x64-rpm.bin
  
Now you should have JDK and JRE 6 installed on your machine. But, still a little thing and the most important, you must know that every time you have to install a software depend to java _yum_ will try to install _Openjdk_ and that is a problem in my case.
The solution is to choose the suitable Java  to the java version which you have installed.
You can find the right one in the web site [scientificlinux.org](http://www.scientificlinux.org) … 

    http://ftp.scientificlinux.org/linux/scientific/5rolling/testing/x86_64/

The last step is to install it .

    yum localinstall ftp://ftp.scientificlinux.org/linux/scientific/5rolling/testing/x86_64/java/java-1.6.0-sun-compat-1.6.0.37-3.sl5.jpp.x86_64.rpm

Finally, you should set up Oracle JDK as your default java package. Then when you installed [tomcat](http://tomcat.apache.org/) for example, it will accept this configuration directly . 

The number of java version which you want to use!

    alternatives  --config java
    java  -version
    javac  -version

And that’s the story of Java compatibility and Linux distributions

If you have any feedback please comment this post . 
