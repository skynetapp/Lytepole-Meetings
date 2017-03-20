#### Step 1:

Function **controlMeetingEditSaveFlow** takes the inputs from the user to edit thee job details, when user clicks on edit in meeting detail view this function will call.

- If login session is not null, function **createEditMeetingInputVO** takes the inputs array and send to data file and prepares the list object.It pepares the input to edit meeting wsdl.
- The above function will be called in action from MeetingData.php which gets the values from input array and sets the values for list value object to pass for
WSDL call. It prepare the query and required input to edit meeting.
- Result returns edit meeting value object array to controller.


#### Step 2:

- Function **editMeeting** used to call the wsdl for edit meeting.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **editMeeting** is used edit meeting the wsdl calls(set_entry).
- Result returns the meeting id to controller.
- Header location will be redirected to meeting detail view based on record id.
