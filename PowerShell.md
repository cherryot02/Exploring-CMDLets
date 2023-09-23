# Introduction to PowerShell
> [!NOTE] 
> These are from my lab works so they are not exactly complete, in an exploration POV. \
> Also, I have no experience in PowerShell so I am being careful not break anything.

## Exploring-CMDLets
I decided to make a table because I find it to be more organized.

| Command     | Description |
| ---         | ---         |
| Get-Command | Typing this on the PowerShell would give you a list of all cmdlets you can do in the Powershell.                                                      |
|             | Within the PowerShell interface, it will display command type, name, version, and source of those commands for PowerShell.                            |

Syntax explored:
```
get-command -type cmdlet
```
which basically just outputs cmdlet command types instead of all of them.
               
| Command      | Description |
| ---          | ---         |
| Show-Command | This cmdlet lets users create a command in another popup window. Once entered in the PowerShell, a pop-up window appears with the list of all the PowerShell the commands. |
|              | This time a user can filter which commands it can show (modules/source or the name). When a command is clicked, there is a short description about it.                     | 
|              | And clicking in show details would further show other forms and parameters a user can specify.                                                                             |

Syntax explored:
```
Show-Command -Name "Invoke-Command"
```

| Command            | Description |
| ---                | ---         |
| Disable-NetAdapter | This cmdlet will disable any network you are connected in, depending on which one you specify.                                                  |
|                    | I actually had a hard time figuring this out because I kept instead of just name according to the table(Get-NetAdapter) but I figured it out.   |

Syntax explored:
```
Disable-NetAdapter -Name "Name of Adapter" -Confirm:$false
```

| Command            | Description |
| ---                | ---         |
| Get-NetIPinterface | This will display a table that shows the IP interface information; IfIndex, address family(IPv4, IPv6), NlMtu(Bytes) and interface metrics.  |

Syntax explored:
```
Get-NetIPInterface -InterfaceIndex 17
```


| Command            | Description |
| ---                | ---         |
| Get-EventLog -List | This displays event logs from the event viewer on the local computer, but it will output just a summarized list of the logs and folders. |

Syntax explored:
```
Get-EventLog -List
```

| Command            | Description |
| ---                | ---         |
| Get-NetIPAddress   | This displays the IP addresses, IPv6, IPv4, IP interfaces of all networks and devices that is within the local network, if not specified.  |

Syntax explored:
```
Get-NetIPAddress -suffixorigin DHCP
```



## END
I come to realise that these codes are not case-sensitive, but it is highly recommended that each new word should be capitalised. 
for example, instead of `get-eventlog -list` , it should be `Get-EventLog -List`. It will execute either way but it's more so for a cleaner and readable code.
I learned this during my web design class. It's also a good habit to get used to.
