#### Step 1:

Function **controlMeetingListFlow** will be called first from index.php to controller. when user clicks on all under jobs in side bar it will call
*this function. From this function we call the wsdl to get the public meetings list and displays.

- Function **createMeetingListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create meeting wsdl
