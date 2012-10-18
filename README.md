project-x
=========

Project X

### Yfrog-API ###

Project to access yfrog Social programmatically from plain Java and Android

#### How to obtain and build ####

##### Pre-requisites #####

You will need to have git v >= 1.7.4 , Java 1.6 and Maven v >= 3.0.3 installed on your development rig.<br/>
Original development was on OS X 10.7.5. There will be little or no difference to develop on Linux,
and for Windows MySysGit is highly recommended, see <code>http://msysgit.github.com</code>

##### Obtainig and Building #####

Clone git project and enter the project home directory:

    $ git clone https://github.com/teosoft123/project-x.git 
    $ cd project-x

Note: all path below presume that current directory is the project home,<br>
the directory created by <code>git clone</code> command. 

Run maven:

    $ mvn clean install

Your build will succeed build phase but fail at the test phase. Now you need to create two users and <add some content>.

##### Adding test users and content #####

You need to add two users <and content for them> to run tests as a part of build.<br>
Each user has to have their own e-mail address.<br>
Create users by going to <code>http://yfrog.com/</code>

##### Telling the build to use your own users #####

Create a file name it 'my-users.properties', without quotes. Add the following content:

    user.1.email: <your user1 e-mail here>
    user.1.password: <your user1 password here>
    
    user.2.email: <your user2 e-mail here>
    user.2.password: <your user2 password here>

Run maven again, this time telling it to use your users:

    $ mvn clean install -Dtest.properties=my-users.properties

This time tests must pass.

#### Android Support ####


The previous build created components most suitable for Java development using maven.<br>
Components created this way do not include any dependencies and delegate dependency management<br>
to build tools such as maven or, in worst case, to the developer.

##### Packaging for Android #####

For better support of Android development community, components created with Android profile package<br>
all the dependencies, including sources of such dependencies, in correspondent jar files.

##### Support for sources for Android development in Eclipse #####

Last but not least feature is support for libs and libsrc forders for Eclipse development.<br> 
Components *.tar.gz and *.zip can be extracted directly into Eclipse Android project home,<br>
creating libs and libsrc directories with jar and sources linked by .properties file that<br>
allows Eclipse with ADT plugin locate and display components sources and their dependencies.<br>
The above source discovery mechanism was verified using Eclipse v3.8 with ADT v20.0.3 on OS X 10.7.5.   

To build the project with the above Android support, run maven as following:

    mvn -P android clean install -Dtest.properties=my-users.properties

