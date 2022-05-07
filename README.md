# a lightweight installer written in C

## Goals
* Small
* Simple

We will release tinysetup as open source project if more than 100 products use it.

## Examples
<pre>; DVDForge's setup script
; please run "tsc setup.tss" in command line to create DVDForge installer.

[Setup]
OutputFile=dvdforge_%v.exe
AppName=DVDForge
AppVersion=%v
AppMutex=DVDForge_Mutex
AppClassName=DVDForgeClass
Publisher=Yubsoft

; use by:
; 1. get shortcut icon
; 2. get exe to run InstallParam: MainExe -i
MainExe=dvdforge.exe

; if 1 install to c:\program files, else c:\program files (x86)
Native64BitApp=1

Compression=lzma
SolidCompression=yes

InstallParam=-xi
UninstallParam=-xu

[Languages]
Default.ini
ChineseSimplified.ini
Italian.ini

[Files]
x86\*=flags:x86
x64\*=flags:x64
language\*.ini=language
license.txt</pre>