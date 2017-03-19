# HelpTips
Checking Which port listening to port 443 and killing the Process

While starting AMMPS and turning ON the Aache Server the issue faced:

port 443 is currently in use.

Below are the steps taken to identify which process was using the port 443 and then killing the process to get relief :)

In the Command Prompt window. 
In Windows machine Start-> Run -> cmd
type netstat -aon. 
This will bring up a list of the ports and list what's listening, established, starting, closing and all other states on them. In this example, look for the one ending in :443 LISTENING

Note down the PID (ProcessID)


Open up the Windows Task Manager (CTRL-ALT-DEL). In order to see the PID numbers of the various processes so you can identify which process is using Port 443, click on the Processes tab, then choose View-->Select Columns from the menu. Check the box next to PID (Process Identifier). You'll now be able to see which process matches up with the PID number you noted earlier. 

Click on the process and click on "End Task"
This should bring the pop up to End the Process.

Try starting the Apache Server Once again.
This should resolve the issue. :)
