#### Step 1:

Function **addMeetingEmployetypeTags** is used to add employee types for the job.

- First we will get the user id by function **getUserID**.
- Function **createEditMeetingTagsInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to meeting tags wsdl.
- In action, above function will be called in MeeetingData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to edit meeting tags.
- The input data will be company, experience ,employmentOptions, meeting id,hourly rate,yearly rate,addintional details.
- Result returns edit meeting tags value object array to controller.


#### Step 2:

- Function **createEditMeetingTags** is used to call the wsdl for create meeting tags.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **createEditMeetingTags** is used send data to wsdl for edit meeting tags and based on the condition wsdl call will be done.
- Result returns tags list array to controller.
- Header location will be redirected to detail view based on the meeting id. 
