#### Step 1:

Function **controlCreateMeetingStep2** is used to save the jobs in steps model step2.
- If job id is null, function **insertNewJobStep1** is executed which is used to call the wsdl for insert new job steps model step 1.
- In action, function **insertNewJobStep1** in NewJobWS.php will get the DB connection and insert the data based on sql query.
- Result returns the inserted job id.

- If job id is not null, function **updateNewJobStep1** is executed which is used to call the wsdl for update new job steps model step 1.
- In action, function **updateNewJobStep1** in NewJobWS.php will get the DB connection and update the data based on sql query and job id.


#### Step 2:

- If Job id is not null, function **getNewJobStep1** is used to call the wsdl for get new job steps model step 1.
- In action, above function will get the DB connection from NewJobWS.php and based on the sql query it returns the id.

#### Step 3:

- Function **showAddJobStep3** takes the input data object and gives to show the create job steps model step3.
- In action, above function will be called which takes the input parameters and will display the tpl page.
- The display shows the step 3 to create a job as **Job_create_step3.tpl** in views folder.


