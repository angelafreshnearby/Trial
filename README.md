User
 - to register new users either by mobile phone
/register
POST
"String (mobile)
"
"Request (8xxxxxxx)
Request (9xxxxxxx)
"
"IF (8xxxxxxxx or 9xxxxxxx), Generate OTP, Send SMS, Return TRUE
ELSE
Return FALSE"
Boolean: True or False value

User
 - to register new users either by google or facebook
/register
POST
"String (email)
String (oauth_platform)"
"Request (abc@gmail.com,facebook)
Request (abc@gmail.com,google SSO)"
"IF GOOGLE SSO or FACEBOOK, Authorize, IF Email Exist, True: return Status Code (1: Login) ; ELSE Return Status Code (2, need OTP)
ELSE Return Status Code (0, fail)
"
"Integer : Status code 
(0:Fail; 1: Login; 2:OTP)"
