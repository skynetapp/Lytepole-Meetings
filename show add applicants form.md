#### Step 1:

Function **showAddApplicantsForm** is used to show applicants create form. when click on add appicants in job detail view and click on 
save button after select the invitees then this function will call.

#### Step 2:

From Groups module we will get the groups list data object array.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.

- Function **getGroupsList** used to call the wsdl call for getting the Group list.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getListArray** in GroupsWS.php is used to send data to wsdl for getting the group list array using the **get_entry_list**.
- Creating the parameters and passing the parameters to wsdl call which returns the groups list result to controller.

- Function **createGroupListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- Result returns the group list array to controller.


#### Step 3:

- Here we will get the user id by function **getUserID**.
- Function **showApplicantCreateForm** akes the input data object and gives to the applicants create form.
- Above function will display the applicant create form tpl page.
- The display tpl page will be **addInvitee.tpl** in views folder.
