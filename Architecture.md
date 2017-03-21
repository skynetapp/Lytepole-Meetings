#### Date: 21/03/2017

#### Description: This document explains the code flow of Meetings.

#### The Folder Structure is as follows:

 Root Directory | Sub Directory 
------------ | -------------
index.php | 
Global | LytepoleWSConnection
Lib | Smarty,nusoap
Modules | Meetings
Views | meetingListFormContact, meetingListFormContactPagination, sharedMeetingsListFormContact, sharedMeetingsListFormContactPagination, meetingPaginationListForm, postedMeetingsListForm, postedMeetingsPaginationListForm, sharedMeetingsListForm, sharedMeetingsPaginationListForm, meetingDetailListForm, meetingConfirmRepayForm, meetingRepayForm, 

#### Architecture

- After login into lytepole, when user clicks on all under jobs in side bar it will call **controlMeetingListFlow**. From this function we call the wsdl to get the public meetings list and displays.
- When we click on referred jobs, function **controlSharedMeetingListContact** will be called. From this function we call the wsdl to get the meetings list posted by that contact and displays.
- When user clicks on Posted under jobs in side bar it will call **controlPostedMeetingListFlow**. From this function we call the wsdl to get the posted meetings list and displays.
- When we click on any of the job to Refer, function **showApplicantCreateForm** will be called which shows the applicants of that job.
- If we want to refer canditates, click on Refer canditates which calls the function **showAddApplicantsForm** where we can select the users to whom we want to refer and onclick save, job will be referred to those canditates.
- If we want to delete the refered canditate, function **controlDeleteApplicant** will be called which is used to delete the invitees form.
- If we want to post a new job, function **showMeetingCreateFormSteps** will be called which shows the creation form steps.
- Function **controlCreateMeetingStep1** is used to save the jobs in steps model step1.


