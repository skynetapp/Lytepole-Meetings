#### Step 1:

Function **controlCreateMeetingStep1** is used to save the jobs in steps model step1.
- If job id is null, function **insertNewJobStep1** is executed which is used to call the wsdl for insert new job steps model step 1.
- In action, function **insertNewJobStep1** in NewJobWS.php will get the DB connection and insert the data based on sql query.
- Result returns the inserted job id.

- If job id is not null, function **updateNewJobStep1** is executed which is used to call the wsdl for update new job steps model step 1.
- In action, function **updateNewJobStep1** in NewJobWS.php will get the DB connection and update the data based on sql query and job id.


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

Here we will get the account data list array to controller from accounts module.

- Function **createAccountListInputVO** will create the object array for input data to send parameters. This function will be called from controller to action.
- Here in action, function takes the input data and prepares the input value object for WSDL from action to AccountData.php.
- Here in AccountData.php, function **createAccountListInputVO** will get the values from input array and sets the values for list value object to pass for WSDL call. It creates the query and required input to create account.

- Function **getAccount** will call the WSDL for account view from controller to action.
- In action, function will call the wsdl call for getting the account details.
- First, it will set the wsdl client by function **setWSDLHandle** from AccountWS.php.
- Next, function **getListArray** will get the account details by ws call **get_entry_list_acc** and returns the result to controller.

- Function **createAccountListDataObjectArr** will create the object array for data list from controller to action.
- Will create the object array for result of wsdl from action to AccountData.php.
- Function **createAccountListDataObject** in AccountData.php will get the values from input array and sets the values for list data object and returns the account object data array to controller.


#### Step 4:

Here we will get the skills from account module.

- Function **getSkills_new** is used to call the wsdl call for getting the account tags.
- First it sets the wsdl client connection and will call wsdl for getting account skills.
- Result returns Account tags list array to controller.


#### Step 5:

- Function **showAddJobStep2** takes the input data object and gives to show the create job steps model step2.
- The above function will display the tpl page of job model step 2.
- The display tpl page will be **Job_create_step2** in views folder.



