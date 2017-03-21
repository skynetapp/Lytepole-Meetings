#### Step 1

Function **controlMeetingRepayFlow** will be called first from index.php to controller. when click on payout in meeting detail and if card is incorrect while creating job then this function call for repayment.

- Function **createMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting wsdl.
- In action, first we will get the user id by function **getUserID**.
- Function **createMeetingListInputVO** in MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting.
- The input parameters will be user id,Module name and Action name,query,sub action, offset.
- Result returns the meeting list value object array.


#### Step 2:

- First we need to get the logged in user id.
- Function **setUnviewedCount** is used to call the wsdl for set view count.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **setUnviewedCount** in MeetingWS.php is used to set unviewed count to wsdl call **set_entry_viewed**.
- Result returns the contact id to controller.


#### Step 3:

- Function **getmeetingList** is used to call the wsdl for getting the public meeting list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getListArray** in MeetingWS.php is used to send data to wsdl for getting the meeting list array using the **get_entry_list_meetings_web**.
- Result returns the meeting list array to controller.

#### Step 4:

- Function **createMeetingListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObject** will be called in MeetingData.php gets the values from input array and sets the values for list data object to pass for create meeting list.
- Result returns meeting data object array to controller.

#### Step 5:

- If count of meeting list data is greater than 0, function **showMeetingConfirmRepaylList** will be called which takes the input data object and shows the repayment confirm form.
- In action, function **showMeetingConfirmRepayView** will be called which displays the confirm repay form tpl page.
- The tpl page will be **meetingConfirmRepayForm.tpl** in views folder.

#### Step 6:

- If count is not greater than 0, header location will be redirected to meetings list.


