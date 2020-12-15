# powershellscript_ms365

Method for using powershell to connect to skype business online(new connection)
(10/1/2020)
•	Kindly use the below link to download and install the Skype for Business connector module and then restart your computer if prompted. 
https://www.microsoft.com/download/details.aspx?id=39366 
•	Open your power shell ISE as Administrator and run the following commands below if your account is not using multifactor authentication. Kindly run this line by line. 
Skype business
Skype for Business Online administrators are responsible for managing policies. Although you can do some of these tasks in the Microsoft 365 admin center, others are easier to do in PowerShell.

1.Set-ExecutionPolicy -ExecutionPolicy unrestricted
2.Import-Module SkypeOnlineConnector
3.$userCredential = Get-Credential
$sfbSession = New-CsOnlineSession -Credential $userCredential
4.Import-PSSession $sfbSession

Teams connection
Install-Module -Name MicrosoftTeams -AllowClobber 
 Import-Module MicrosoftTeams
 Connect-MicrosoftTeams
