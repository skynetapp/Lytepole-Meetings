#### Step 1:

Function **controlMeetingDetailViewFlow** will be called first from index.php to controller. This function calls when we click on meeting detail in jobs list view.

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

- Function **getmeetingListDetail** is used to call the wsdl for getting the meeting detail view list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getMeetingListDetail** in MeetingWS.php is used to send data to wsdl for getting the meeting detailview.
- The wsdl call **get_entry_list_meetings_detail_web** is passed to created parameters.
- Result returns meeting list array.


#### Step 4:

- Function **createMeetingListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObject** will be called in MeetingData.php gets the values from input array and sets the values for list data object to pass for create meeting list.
- Result returns meeting data object array to controller.

#### Step 5:

- If count of meeting list data is greater than 0, function **showMeetingDetailList** will be called which takes the input data object and gives the meeting detail list view .
- In action, function **showMeetingDetailListView** will be called which displays the detail list view tpl page.
- The tpl page will be **meetingDetailListForm.tpl** in views folder.

#### Step 6:

- If count is not greater than 0, header location will be redirected to meetings list.



