#### Step 1:

Function **controlEditPrivacySaveFlow** will be called when privacy save.

- In action, first we will set the wsdl client connection by function **setWSDLHandle**.
- Function **setMeetingPrivacy** is used to set meeting privacy by wsdl call **set_entry**.
- Result returns the meeting id to controller.
- Header location will be redirected to detail view with meeting id.
