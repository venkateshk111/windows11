# windows11
Windows 11 settings and troubleshooting

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
 
## Disable snipping tool on Windows 11
[https://www.makeuseof.com/windows-11-disable-snipping-tool/](https://www.makeuseof.com/windows-11-disable-snipping-tool/)
