# nosleep
Simple Windows HTA script to prevent the lock screen
## screenshot
![screenshot1](https://github.com/pemn/nosleep/blob/master/assets/screenshot1.png)
## Use cases
The only sensible use case is for computers with a enterprise policy that enforces the lock screen after a period of inactivity (usually 120 seconds).  
## Alternative
If this is not your case, the better solution is just configuring the lock screen time to a larger number like 1 hour. This setting is disabled by default in Windows 10 but can be enabled again setting a registry key.  
Ex.: run powershel as administrator and enter:  
`set-itemproperty -Path Registry::HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\7516b95f-f776-4464-8c53-06167f40cc99\8EC4B3A5-6868-48c2-BE75-4F3044BE88A7 -Name Attributes -Value 2`  
After changing this settings the option to change the lock screen timeout will appear in advanced energy settings, change energy plan:  
![energy_settings](https://github.com/pemn/nosleep/blob/master/assets/energy_settings.png)
## License
This code is released in the Public Domain and may be freely used, copied, distributed and changed.
