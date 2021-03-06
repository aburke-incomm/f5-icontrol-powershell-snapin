Thanks for taking a look at the iControl PowerShell SnapIn.

-------------
 Installation
-------------
For the first time use, you will have to run the included setupSnapIn.ps1 in the c:\program files\F5 Networks directory from within PowerShell.

PS: c:\program files\f5 networks> .\setupSnapIn.ps1

-------------
 Running
-------------
Once you've installed the SnapIn into PowerShells SnapIn directory, you can instantiate the SnapIn as follows

PS: > Add-PSSnapIn -iControlSnapIn

Now, the SnapIn is loaded into the runtime.  You can now make iControl calls.  To get a list of all the iControl CmdLets, you can use the following Cmdlet.

PS: > Get-iControlCommands

This will list all available iControl Cmdlets included in the iControlSnapIn.  Before making any of the other calls, you will have to initialize the iControl connection to the BIG-IP with the Initialize-iControl Cmdlet.

PS: > Initialize-iControl -Hostname <bigip_address> -Credentials (Get-Credential)

This will prompt with a dialog box for the connection credentials.  If you prefer to pass them in in clear text, you can use the following optional parameters

PS: > Initialize-iControl -Hostname <bigip_address> -Username <username> -Password <password>

Now, just give them all a shot.  Remember you can always use autocomplete to find out the parameters for each cmdlet.