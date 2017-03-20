#### Step 1:

Function **controlMeetingEditFlow** will be called when cwe lick on edit on meeting detail.

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

- Function **createMeetingListDataObjectEdit** creates a list object array for the data get from wsdl and passes to view page.
- The above function gets the values from input array and sets the values for list data object to pass for edit meeting list.
- Result returns the edit meeting data object array.


#### Step 4:

- Function **getmeetingListTags** is used to call the wsdl for get meeting tags list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getmeetingListTags** is used to send data to wsdl for getting the meeting tags by wsdl call **get_entry_list_tags**.
- Result returns the tags list array to controller.


#### Step 5:

- Function **createMeetingTagsListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- Above function in MeetingData.php gets the values from input array and sets the values for list data object to pass for create meeting tags
- Result returns the meeting tags object array to controller.


#### Step 6:

- If the count of tags is greater than 0, function **showMeetingEditView** will be called which takes the input data object and shows the meeting edit form.
- The above function in MeetingView.php will display the edit meeting form tpl page as **newEditMeetingForm.tpl**.
- 




