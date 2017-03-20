#### Step 1:

Function **controlDeleteMeetingFlow** is used when we click on delete in meeting detail.

- Function **deleteMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to delete meeting wsdl.
- In action, function **deleteMeetingListInputVO** gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to delete meeting.
- Result returns delete meeting value object array.


#### Step 2:

- Function **deleteMeeting** takes the input value object and passes to the wsdl call to delete a meeting.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **deleteMeeting** is used to delete meeting the wsdl calls(set_entry).
- The header location will be redirected to meeting list.
