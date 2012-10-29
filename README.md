### Yfrog-API ###
=========

Project to access yfrog Social programmatically from plain Java and Android

##### Pre-requisites #####

You will need to have git v >= 1.7.4, eclipse with ADT plugin and Java 1.6 installed on your development computer.<br/>
Original development was on OS X 10.7.5. There will be little or no difference to develop on Linux,
and for Windows MySysGit is highly recommended, see <code>http://msysgit.github.com</code>

##### Obtainig and Building #####

Clone git project and enter the project home directory:

    $ git clone https://github.com/teosoft123/project-x.git 
    $ cd project-x

Note: all paths below presume that current directory is the project home,<br>
the directory created by <code>git clone</code> command. 

Import projects into eclipse using File, Import, Existing Projects into Workspace

Navigate to project home directory. There are two projects, yfrog-api-android and yfrog-examples.

##### Requesting Application ID #####

To use Yfrog API, every application requires Application ID. You can request your application ID here:
 
    http://yfrog.com/app_id_request/
    
##### Development

You can see an example of Android application that logs on to user account in <code>yfrog-examples</code> project.
See file API.md to more details on how to use Yfrog APIs. 
