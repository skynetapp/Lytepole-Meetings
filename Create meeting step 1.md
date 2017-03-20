#### Step 1:

Function **controlCreateMeetingStep1** is used to save the jobs in steps model step1.
- If job id is null, function **insertNewJobStep1** is executed which is used to call the wsdl for insert new job steps model step 1.
- In action, function **insertNewJobStep1** in NewJobWS.php will get the DB connection and insert the data based on sql query.
- Result returns the inserted job id.

- If job id is not null, function **updateNewJobStep1** is executed which is used to call the wsdl for update new job steps model step 1.
- In action, function **updateNewJobStep1** in NewJobWS.php will get the DB connection and update the data based on sql query and job id.


#### Step 2:

