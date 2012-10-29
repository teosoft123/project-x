Detailed API Documentation
===

#### Yfrog User and Messaging API 

All messaging operations are performed using an instance of a class Yfrog:

    Yfrog api = Yfrog.getInstance();
    
All media-related operations are performed using an instance of a class YfrogMedia:

YfrogMedia mediaApi = YfrogMedia.getInstance();    

To start using Yfrog Social, login first

    api.login(<email>, <password>, <application-id>);

Login creates a cookie that is used for all following methods calls.

To obtain a logged on user timeline called Feed:

    Feed userFeed = api.getOwnerMessages(Group.FRIENDS, 100);

To comment on a message:

    
To post a new message with an image:

    ImageMetadata im = mapi.uploadImage(Group.FAMILY, imageFile);
    String imageId = im.getImageId();
    m = Message.create("Test message from yfrog Social Java API", Group.FRIENDS, Privilege.SOCIAL, Arrays.asList(imageId));
    messageId = api.post(m);
     
<!--
<table>
<tr><th>name</th><th>required</th><th>description</th></tr>
<tr><td>login</td><td>yes</td><td>desc here</td></tr>
</table>
-->

#### Yfrog Media API 
