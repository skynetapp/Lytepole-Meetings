#### Step 1:

Function **showSendEmailFormContact** is used to send email to contact. when click on email in contact detail view this function will call.

- 
- Function **createContactListInputVO** in contacts module will create the value objects from controller to action.
- In action, user id will be set by function **getUserID**.
- Function **createContactListInputVO** will be called in action from ContactsData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It will prepare the query and required input to create contact.
- The list value object array result will be returned to controller.

#### Step 2:

- Function **getContactsList** is used to call the wsdl call for getting the contacts list from controller to action.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **getListArray** in ContactsWS.php which is used send data to wsdl for getting the contacts list array using the ws call **get_entry_list_con**.
- The contacts list array result will be returned to controller.

#### Step 3:

- Here we will get the user id.
- Function **getAccountEmail** will be called from accounts module which is used to get the emails related to account.
- Function **createMeetingListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createMeetingListDataObject** will be called in MeetingData.php gets the values from input array and sets the values for list data object to pass for create meeting list.
- Result returns meeting data object array to controller.

#### Step 4:

- Function **showSendEmailFormContact** takes the input data object and gives to the contact send mail form.
- The above function will display the email contact form as tpl page.
- The tpl page will be **showSendEmailFormContact** in views folder.
