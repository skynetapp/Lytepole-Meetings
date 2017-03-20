#### Step 1:

Function **controlChangeApplicantStatus** is used when we click on status on invitees and save.

- Function **createChangeInviteeStatusInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting invitee status change wsdl.
- In action, above function will be called from MeetingData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to change invitee status.
- Result returns invitee status value object array to controller.

#### Step 2:

- Function **changeInviteeStatus** is used to call the wsdl for change invitee status.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **changeInviteeStatus** is used change invitee status the wsdl calls(set_entry).
- Result returns the invitee id to controller.
- If the status error is true, the invitee status will be true or else it will be false.
