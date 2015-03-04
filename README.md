# Apache_Server_Help
I was having trouble starting my Apache Server through XAMPP Control Panel with my PC...Here's how I fixed it.

I was receiving errors that looked like this:
2:11:21 PM  [Apache] 	Error: Apache shutdown unexpectedly.
2:11:21 PM  [Apache] 	This may be due to a blocked port, missing dependencies, 
2:11:21 PM  [Apache] 	improper privileges, a crash, or a shutdown by another method.
2:11:21 PM  [Apache] 	Press the Logs button to view error logs and check
2:11:21 PM  [Apache] 	the Windows Event Viewer for more clues
2:11:21 PM  [Apache] 	If you need more help, copy and post this
2:11:21 PM  [Apache] 	entire log window on the forums

I looked up "how to" on this link:
https://community.apachefriends.org/f/viewtopic.php?f=16&t=69784&sid=6722e9968dac6848099dce5992af4c2b

And followed these directions:
  ~ rightclick your xampp-control.exe file
  ~ choose "run as Administraor"
  ~ if UAC is enabled you need to confirm that you really want to run as Administrator
  ~ if you are not logged in as Administrator on your Windows system you need to type in the credentials of an administrator
  
but when I right clicked on the xampp-control.exe file, there was no "run as Administrator" option. 
(the xampp-control.exe can be found in the "Process" tab of your Task Manager. Ctr+Alt+Del then select "Start Task Manager" to find it.)
I did, however, find "run as Administrator" when I right clicked on the the XAMPP Control Panel icon in it's directory.

After I ran the program as Administrator, The green check marks to the very left of the Apache, MySQL, and FileZilla "start" buttons
were now red "x" marks. I right clicked on the check marks and it asked if I wanted to install them. I said yes. I then saw the following
errors:
2:13:14 PM  [Apache] 	Problem detected!
2:13:14 PM  [Apache] 	Port 80 in use by "C:\Program Files\Skype\Phone\Skype.exe" with PID 1060!
2:13:14 PM  [Apache] 	Apache WILL NOT start without the configured ports free!
2:13:14 PM  [Apache] 	You need to uninstall/disable/reconfigure the blocking application
2:13:14 PM  [Apache] 	or reconfigure Apache and the Control Panel to listen on a different port
2:13:14 PM  [Apache] 	Problem detected!
2:13:14 PM  [Apache] 	Port 443 in use by "C:\Program Files\Skype\Phone\Skype.exe" with PID 1060!
2:13:14 PM  [Apache] 	Apache WILL NOT start without the configured ports free!
2:13:14 PM  [Apache] 	You need to uninstall/disable/reconfigure the blocking application
2:13:14 PM  [Apache] 	or reconfigure Apache and the Control Panel to listen on a different port

So I uninstalled Skype and now it works. For now, at least. This was my experience. Hopefully it's helpful for someone else.




