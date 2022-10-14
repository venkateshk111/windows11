# windows11
Windows 11 settings and troubleshooting

## Windows profile user name
https://answers.microsoft.com/en-us/windows/forum/all/windows-profile-user-name/c660f8da-a1fe-40ce-b8be-5a83e4de6448
https://www.tenforums.com/tutorials/89060-change-name-user-profile-folder-windows-10-a.html

## How to ungroup icons on taskbar in Windows 11
https://github.com/valinet/ExplorerPatcher/releases

## Enabling Group Policy Editor (gpedit.msc)
1. Create a batch file with follwing content and execute it.
```
 @echo off
 pushd "%~dp0"
 dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt
 dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt
 for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"
 pause
 ```
 
 Ref: [https://windowsreport.com/windows-cannot-find-gpedit-msc-windows-11/](https://windowsreport.com/windows-cannot-find-gpedit-msc-windows-11/)

## Disable snipping tool on Windows 11 (not so effective )
[https://www.makeuseof.com/windows-11-disable-snipping-tool/](https://www.makeuseof.com/windows-11-disable-snipping-tool/)

## Disk Partition Calculator
https://windowspro.eu/windows-partition-calculator-install/

## Disk Partition
https://support.lenovo.com/in/en/solutions/ht505250-how-to-reduce-or-expand-system-partition-c-drive-size-in-windows
