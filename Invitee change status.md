#### Step 1:

Function **controlInviteeStatusChange** is used to show applicants create form, when click on add appicants in job detail view and click on save button after select the invitees then this function will call.

- If the login session is not null, function **createInviteeStatusInputVO** will be called which takes the values from input array and sets the value object.
- In action, above function will be called which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create invitee status.
- The input values are login_session,inviteeid,meetingid,status,description.
- Result returns create invitee status value object array to controller.


#### Step 2:

- Function **setInviteeStatus** is used to call the wsdl for set meeting invitee staatus.
- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **setInviteeStatus** is used to set invitee status the wsdl calls(set_entry_viewed).
- Result returns the invitee id to controller.


#### Step 3:

- If the **status == Hired** and **referralfee == 1**, function **showApplicantStatusHireForm** takes the input data object and gives to show the applicant status hire form.
- In action, above function will be called in MeetingView.php which shows the applicant status hire form tpl page.
- The display tpl page will be **ApplicantHiredConfirm** in views folder.


#### Step 4:

- If the **status != Hired**, header location will be redirected to Applicant view based on the meeting id.
