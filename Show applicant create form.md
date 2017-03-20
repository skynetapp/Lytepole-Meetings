#### Step 1:

Function **showApplicantCreateForm** is used to show applicants create form. This function will be called when we click on add appicants in job detail view.

- Function **createInviteeListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting invitees wsdl.
- Above function in MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to invitee list.
- Result returns invitee list value object array to controller.


#### Step 2:

- Function **getInviteeList** is used to call the wsdl for getting the meeting invitee list.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **getInviteeList** is used send data to wsdl for getting the invitee list array using the **get_entry_list**.
- Result returns the invitee list array to controller.

#### Step 3:

- Function **createInviteeListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, above function gets the values from input array and sets the values for list data object to pass and to create invitees list.
- Result returns inviteees list data object array to controller.


#### Step 4:

- Here we will get the user id by function **getUserID**.
- Function **showApplicantForm** takes the input data object and gives to the applicants form.
- In action, above function will be called which displays the applicants view form tpl page.
- The display tpl page will be **ApplicantsViewForm.tpl** in views folder.
