# nosleep
Simple Windows HTA script to prevent the lock screen. It works by sending ("typing") a unimplemented key (F15) every 60 seconds.  
Most keyboards only have F keys up to F12 so this can be run all the time without risk of disrupting anything.  
It is a javascript application, so while Windows will treat it as a executable.  
The source code can be inspected in any text editor (No binary black box which you are not sure can be trusted).
## screenshot
![screenshot1](./assets/screenshot1.png?raw=true)  
![screenshot2](./assets/screenshot2.png?raw=true)  
## Setup Automatic Startup
After executing the app any time, you have the option to "install" it by clicking on the lower right floppy disk 🖫 button.  
You will be prompted if you want to setup so the app is automatically launched it every time you log in. CLick OK to proceed or Cancel.  
You can remove this startup by clicking again on the same button, which now instead of a floppy disk 🖫 should have a bomb 💣 icon.  
This startup link will point to the current file path of the executable, so if you move it to another folder be sure to repeat this setup. The link is stored on the Windows Startup folder.
## Use cases
The only sensible use case is for corporate computers with the enterprise policy that enforces the lock screen after a period of inactivity (usually 60 to 120 seconds).  
## Alternative
If this is not your case, the better solution is just configuring the lock screen time to a larger number like 1 hour. This setting is disabled by default in Windows 10 but can be enabled again setting a registry key.  
Ex.: run powershel as administrator and enter:  
`set-itemproperty -Path Registry::HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\7516b95f-f776-4464-8c53-06167f40cc99\8EC4B3A5-6868-48c2-BE75-4F3044BE88A7 -Name Attributes -Value 2`  
After changing this registry setting, the option to change the lock screen timeout will appear in advanced energy settings - change energy plan:  
![energy_settings](https://github.com/pemn/nosleep/blob/master/assets/energy_settings.png)
## License
This code is released in the Public Domain and may be freely used, copied, distributed and changed.
