#### Step 1:

Function **controlChangeApplicantStatusPublic** is used to change job type(public or private).

- First we will get the user id by function **getUserID**.
- Function **changeInviteeStatusPublic** is used to call the wsdl for set meeting type.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **changeInviteeStatusPublic** is used to send data to wsdl to change invitee status.
- Based on the conditions, it will call the wsdl and will return the result.  
- If the status error is true, the invitee status will be true or else it will be false.
