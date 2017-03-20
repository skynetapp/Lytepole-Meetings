#### Step 1:

Function **controlSharedMeetingListFlow** will be called first from index.php to controller. when user clicks on jobs inbox under jobs in side bar it will call this function. From this function we call the wsdl to get the shared meetings list and displays.

- Function **createMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting wsdl.
- In action, first we will get the user id by function **getUserID**.
- Function **createMeetingListInputVO** in MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting.
- The input parameters will be user id,Module name and Action name,query,sub action, offset.
- Result returns the meeting list value object array.


#### Step 2:

- Function **getSharedMeetingsList** is used to call the wsdl for getting the shared meeting list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getSharedMeetingsListArray** is used send data to wsdl for getting the shared meeting list array using the **get_user_meetings_shared_web**.
- Result returns shared meeting list array to controller.


#### Step 3:

- Function **createMeetingListDataObjectArrNew** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObjectNew** gets the values from input array and sets the values for list data object to pass to create meeting list.
- Input parameters list will be next offset,query,query date,entry,id name ,loaction, company,skills, experience.
- Result returns the meeting data object array to controller.

#### Step 4:

- Get the user id by function **getUserID**.
- Function **getBadgeCount** is used to call the wsdl for getting the meeting badge count.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getBadgeCount** in MeetingWS.php will get the input data and will send data to wsdl **get_entries_count**.
- Result reutrns the badge count to controller.


#### Step 5:

- If **ajaxcall == yes**, function **showSharedMeetingsPaginationList** takes the input data object and gives to the shared meeting Pagination list view.
- In action, function **showSharedMeetingsPaginationListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **sharedMeetingsPaginationListForm.tpl** in views folder.


#### Step 6:

- If **ajaxcall != yes**, function **showSharedMeetingsList** takes the input data object and gives the shared meeting list view.
- In action, function **showSharedMeetingsListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **sharedMeetingsListForm.tpl** in views folder.



