#### Step 1:

Function **controlSaveRatingFlow** will be called first from index.php to controller which is used to save rating for job.

- First we will get the user id by calling function **getUserID**.
- Function **createAddRatingMeetingInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to meeting rating wsdl.
 action, function **createMeetingListRatingDataObjectNew** gets the values from input array and sets the values for list data object to pass to create meeting list.
- Input parameters list will be name,from_userid,to_userid,job_sugarid,rating,deleted,rating_type,description,assigned_user_id.
- Result returns the Message rating list data object array to controller.


#### Step 2:

- Function **saveRating** is used to call the wsdl for set rating for meeting.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **saveRating** in MeetingWS.php is used send data to wsdl for getting the messages list array using the **get_entry_list**.
- Result returns the rating id list array to controller.


#### Step 3:

- If **rating_type == applicant_rating**, header location will redirect to the action as **ApplicantView** which shows the meeting appicants view.
- Else header location will redirect to **DetailView** shows the job detail view.
