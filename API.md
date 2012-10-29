### How-To API Documentation

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
    
To post a new message with one image:

    ImageMetadata im = mapi.uploadImage(Group.FAMILY, imageFile);
    String imageId = im.getImageId();
    Message m = Message.create("Test message from yfrog Social Java API", Group.FRIENDS, Privilege.SOCIAL, Arrays.asList(imageId));
    String messageId = api.post(m);
    
To upload multiple images, pass a List of image IDs as a last parameter.

To get the message by ID:

    MessageThread mt = api.getMessage(messageId);
     
To comment on a message:

    String replyId = api.comment(mt, "This is a reply");

#### Yfrog Media API

To post messages with images you need to upload images first.
To upload an image with family group permission:

    File imageFile = new File(<your file name>);
    ImageMetadata im = mediaApi.uploadImage(Group.FAMILY, imageFile);
 

<!--
<table>
<tr><th>name</th><th>required</th><th>description</th></tr>
<tr><td>login</td><td>yes</td><td>desc here</td></tr>
</table>
-->

