#### Step 1:

Function **controlAddInvitees** is used to show applicants create form. when click on add appicants in job detail view and click on 
save button after select the invitees then this function will call.

- If the login session is not null, function **createAddMeetingInviteesInputVO** takes the inputs array and send to data file and prepares the list object
It pepares the input to create meeting invitees wsdl.
- The above function in MeetingData.php will set the data which returns the meeting invitees object array to controller.


#### Step 2:

- Function **createMeetingInvitees** takes the input value object and passes to the wsdl call to create a meeting invitees.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **createMeetingInvitees** is used create a meeting invitees and set relation with meeting the wsdl calls(set_entry).
- Result returns the relation id.
- Header location will be redirected to applicant create form and record id.
