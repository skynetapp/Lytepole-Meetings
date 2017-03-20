#### Step 1:

Function **showSendEmailForm** is used send email to job poster, when click on email in job detail view this function will call.

- Function **createMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting wsdl.
- In action, first we will get the user id by function **getUserID**.
- Function **createMeetingListInputVO** in MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting.
- The input parameters will be user id,Module name and Action name,query,sub action, offset.
- Result returns the meeting list value object array.


#### Step 2:

- Function **getmeetingList** is used to call the wsdl for getting the public meeting list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getListArray** in MeetingWS.php is used to send data to wsdl for getting the meeting list array using the **get_entry_list_meetings_web**.
- Result returns the meeting list array to controller.

#### Step 3:

- Here we will get the user id.
- Function **getAccountEmail** will be called from accounts module which is used to get the emails related to account.
- Function **createMeetingListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObject** will be called in MeetingData.php gets the values from input array and sets the values for list data object to pass for create meeting list.
- Result returns meeting data object array to controller.

#### Step 4:

- Function **showSendEmailFormNew** takes the input data object and gives to the meeting send mail form.
- In action, function **showSendEmailFormViewNew** will be called from MeetingView.php which displays the email form view tpl page.
- The display tpl page will be **showSendEmailFormNew** in views folder.
