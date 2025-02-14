Sim800L Arduino Library revised
=====


The purpose of this library is to simplify and speed up the use of the SIM800L module for Arduino.



Contributions
---

I'm currently looking for more collaborators - feel free to submit your pull request to grow this open-source project!



Connections
---


Arduino      |   Sim800L        |    Notes  
-------------|------------------|------------
+5v| (3.8v)~(4.4v)!| Power supply input
10 RX_PIN | TX |  
11 TX_PIN | RX |
2   RESET_PIN | RST| Reset Pin
GND | GND | 


Functions
---


Name|Return|Notes
:-------|:-------:|:-----------------------------------------------:|
begin()|None|Initialize the library
begin(number)|None|Initialize the library with user's baud rate
reset()|None|Reset the module, and wait to Sms Ready.
setSleepMode(bool)|bool|enable or disable sleep mode. If it returns true, there is an error.
getSleepMode()|bool|return sleep mode status. If it returns true, there is an error.
setFunctionalityMode(number)|bool|set functionality mode. If it returns true, there is an error.
getFunctionalityMode()|bool|return functionality mode status. If it returns true, there is an error.
setPIN(String)|bool|enable user to set a pin code. If it returns true, there is an error.
getProductInfo()|String|return product identification information
getOperatorsList()|String|return the list of operators
getOperator()|String|return the currently selected operator
calculateLocation()|bool|calculate gsm position. If it returns true, there is an error.
getLocationCode()|String|return the location code
getLongitude()|String|return longitude
getLatitude()|String|return latitude
sendSms(number,text)|bool|both parameters must be Strings. If it returns true, there is an error.
readSms(index)|String|index is the position of the sms in the prefered memory storage
getNumberSms(index)|String|returns the number of the sms.
delAllSms()|bool|Delete all sms. If it returns true, there is an error.
signalQuality()|String|return info about signal quality
answerCall()|bool| If it returns true, there is an error.
callNumber(number)|None|
hangoffCall()|bool| If it returns true, there is an error.
getCallStatus()|uint8_t|Return the call status, 0=ready,2=Unknown(),3=Ringing,4=Call in progress
setPhoneFunctionality()|None|Set at to full functionality 
activateBearerProfile()|None|
deactivateBearerProfile()|None|
RTCtime(int *day,int *month, int *year,int *hour,int *minute, int *second)|None| Parameters must be reference ex: &day
dateNet()|String|Return date time GSM
updateRtc(utc)|bool|Return if the rtc was update with date time GSM. 
____________________________________________________________________________________



Credits
---


Original version of the library by:   [Cristian Steib] (https://github.com/cristiansteib)
