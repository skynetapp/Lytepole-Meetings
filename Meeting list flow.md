#### Step 1:

Function **controlMeetingListFlow** will be called first from index.php to controller. when user clicks on all under jobs in side bar it will call this function. From this function we call the wsdl to get the public meetings list and displays.

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

- Function **createMeetingListDataObjectArrNew** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObjectNew** gets the values from input array and sets the values for list data object to pass to create meeting list.
- Input parameters list will be next offset,query,query date,entry,id name ,loaction, company,skills, experience.
- Result returns the meeting data object array to controller.


#### Step 4:

- If **ajaxcall == yes**, function **showMeetingPaginationList** takes the input data object and gives to the meeting list view pagination.
- In action, function **showMeetingPaginationListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **meetingPaginationListForm.tpl** in views folder.


#### Step 5:

- If **ajaxcall != yes**, function **showMeetingList** takes the input data object and gives to the meeting list view.
- In action, function **showMeetingListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **meetingListForm.tpl** in views folder.



