#### Step 1:

Function **controlPostedMeetingListFlow** will be called first from index.php to controller. when user clicks on posted under jobs in side bar it will call
*this function. From this function we call the wsdl to get the posted meetings list and displays.

- Function **createMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting wsdl.
- In action, first we will get the user id by function **getUserID**.
- Function **createMeetingListInputVO** in MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create meeting.
- The input parameters will be user id,Module name and Action name,query,sub action, offset.
- Result returns the meeting list value object array.


#### Step 2:

- Function **getPostedMeetingsList** is used to call the wsdl for getting the posted meeting list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getPostedMeetingsListArray** in MeetingWS.php is used send data to wsdl for getting the posted meeting list array using the **get_user_meetings_posted_web**.
- The input parameters will be session id, module name,query,orderby,offset,max result,deleted.
- Result returns posted meeting list array to controller.

#### Step 3:

- Function **createMeetingListDataObjectArrNew** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObjectNew** gets the values from input array and sets the values for list data object to pass to create meeting list.
- Input parameters list will be next offset,query,query date,entry,id name ,loaction, company,skills, experience.
- Result returns the meeting data object array to controller.


#### Step 4:

- If **ajaxcall == yes**, function **showPostedMeetingsPaginationList** takes the input data object and gives to the posted meeting list view pagination.
- In action, function **showPostedMeetingsPaginationListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **postedMeetingsPaginationListForm.tpl** in views folder.


#### Step 5:

- If **ajaxcall != yes**, function **showPostedMeetingsList** takes the input data object and gives to the posted meeting list view.
- In action, function **showPostedMeetingsListView** will be called from MeetingView.php which displays the jobs list tpl page.
- The display tpl page will be **postedMeetingsListForm.tpl** in views folder.

