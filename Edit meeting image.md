#### Step 1:

Function **editMeetingImage** is used to update the meeting image, and uploads to sugar folder using curl.

- Function **createMeetingImagesListInputVO** takes the inputs array and send to data file and prepares the list object.It prepares the input to meeting image wsdl.
- In action, function **createMeetingImageListInputVO** will be called from MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting image.
- The input parameters are login_session,record id,action,image,user id.
- Result returns create meeting image value object array to controller.


#### Step 2:

- Function **editmeetingImages** is used to call the wsdl for edit meeting image.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **editMeetingImage** in MeetingWS.php is used to edit meeting image by wsdl call **set_entry**.
- Result returns the meeting id to controller.


#### Step 3:

- Function **createmeetingImagesRelation** takes the input value object and set relation between iamge and meeting.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **createMeetingImageRelation** is used create a relation between meeting and image the wsdl calls(set_relationship).
- Result returns the relation id  to controller.

#### Step 4:

- Curl call will be executed here with the execution of curl. The curl process will check if it is false error message will be displayed.
- If the curl process is true, **operation completed without any errors** will be displayed.
- Header location will be redirected to meeting detail view based on the id.
