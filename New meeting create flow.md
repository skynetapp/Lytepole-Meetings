#### Step 1:

Function **controlNewMeetingCreateFlow** will be called first from index.php to controller which is used to save the jobs.

- First we will get the uer id by function **getUserID**.
- Function **createAddNewMeetingInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to  create meeting wsdl.
- In action, the above function from MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create new meeting.
- Result returns the meeting value object array.

#### Step 2:

- Function **createNewMeeting** takes the input value object and passes to the wsdl call to create a meeting.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **createNewMeeting** in MeetingWS.php is used create a new meeting using the wsdl calls(set_entry).
- Result returns the meeting id.

#### Step 3:

- If the amount and card number is not null, function **createMeetingPaymentInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to meeting payment.
- Above function gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting payment.
- Result returns create meeting payment value object array to controller.

#### Step 4:

- Function **createMeetingPayment** used to call the wsdl for payment send and payment get history.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getPaymetHistory** is used send data to wsdl for getting the payment history.
- The wsdl call will be **get_entry_list** which returns the payment list array.
- Header location will be redirected to posted meeting list.



