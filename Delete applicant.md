#### Step 1:

Function **controlDeleteApplicant** is used to delete the invitees form.

- Function **deleteApplicant** is used to call the wsdl for set delete invitee.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **deleteApplicant** is used change delete applicants the wsdl calls(set_entry) and returns the result as invitee id.
- Header loaction will be redirected to applicant list form.
