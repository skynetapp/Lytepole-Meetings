#### Step 1:

Function **controlNewMeetingCreateFlow** will be called first from index.php to controller which is used to save the jobs.

- First we will get the uer id by function **getUserID**.
- Function **createAddNewMeetingInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to  create meeting wsdl.
- In action, the above function from MeetingData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create new meeting 
