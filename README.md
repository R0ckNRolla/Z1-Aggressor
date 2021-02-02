# Z1-AggressorScripts

![](https://img.shields.io/badge/Z1-AggressorScripts-red.svg) ![](https://img.shields.io/github/languages/top/z1un/Z1-AggressorScripts. svg) ![](https://badgen.net/github/stars/z1un/Z1-AggressorScripts)

Applicable to Cobalt Strike 3.x & 4.x plug-ins.


2020.12.20 update:

-Update [fscan](https://github.com/shadow1ng/fscan) tool.

2020.11.21 update:

-The zip package of the auxiliary module is replaced with [SharpZip](https://github.com/uknowsec/SharpZip) of Master uknow, and the memory is loaded without uploading.
-The permission maintenance module is newly added to create a self-startup operation, including three ways to add a registry, add a startup folder, and create a startup service.

2020.11.20 update:

-Intranet penetration module added support for nps.

-Frp is changed from the previous compressed version of upx to the uncompressed version. Both frp32-bit and nps compressed by upx will report the virus in 360, and all will be replaced with the original version. However, this project has increased the volume from a few megabytes to a few 30 megabytes. It is strongly recommended to download the release compressed file from [gitee](https://gitee.com/z1un/Z1-AggressorScripts).

  Windows-npc64 bit will report an error after it is uploaded via cs. I don't know if it is my personal environment problem, so npc only uploads 32 bits, which does not affect the use.

  

![image-20201119120243146](https://oss.zjun.info/zjun.info/20201119120244.png)




## escalation

1. [watson](https://github.com/rasta-mouse/Watson) Get extractable vulnerabilities
2. [sweetpotato](https://github.com/CCob/SweetPotato)
3. juicypotato
4. MS14-058
5. MS15-051
6. MS16-016
7. MS16-032
8. MS16-135
9. CVE-2020-0796
10. [SharpBypassUAC](https://github.com/FatRodzianko/SharpBypassUAC)

## Information Collection

1. Common commands for stand-alone
   -systeminfo
   -whoami /all
   -ipconfig /all
   -View routing table
   -View arp cache
   -View user information
   -View installer and version information
   -View installed patches
   -View running processes and paths
   -View process details
   -View services
   -View firewall configuration
   -View scheduled tasks
   -View launcher information
   -View online users
   -View boot time
   -View historical commands of powershell v5
   -View recently used items
   -View SMB pointing path

2. Common commands in domain environment
   -[AdFind](http://www.joeware.net/freetools/tools/adfind/index.htm)
     -List domain controller names
     -Query online computers in the current domain
     -Query online computers in the current domain (only display name and operating system)
     -Query all computers in the current domain
     -Query all computers in the current domain (only display name and operating system)
     -Query all users in the domain
     -Query all GPOs
   -Query domain
   -View domain management
   -View domain user details
   -View current login domain
   -View time server
   -Display a list of computers in the current domain
   -View the domain management of the local machine
   -View all domain users
   -View the list of all user groups in the domain
   -View the primary domain controller
   -View domain control list
   -View domain controller hostname
   -Get domain trust information
   -Get domain password information
   -View a list of all domain member computers
   -View all computers in the domain

3. [SharpChassisType](https://github.com/RcoIl/CSharp-Tools/tree/master/SharpChassisType) Determine the host type

   ```
   Used to determine the current machine type (desktop computer, notebook, etc.).
   ```

4. [SharpNetCheck](https://github.com/uknowsec/SharpNetCheck) detects out of the network

   ```
   During the infiltration process, there is a great desire for machines that can go out of the network. In the case of collecting a large number of weak passwords, it is too troublesome to test whether one can go out of the network one by one. So there is this tool, which can be used with horizontal tools such as wmiexec, psexec and other horizontal tools to perform batch detection. This tool can echo the intranet ip address and computer name in dnslog, which can realize the rapid positioning of outbound machines in the intranet.
   ```

5. [SharpEventLog](https://github.com/uknowsec/SharpEventLog)(Get system login log, quickly locate operation and maintenance machine)

   ```
   Read all computer information that has failed to log in to this machine or successfully logged in (4624, 4625), and quickly locate operation and maintenance managers in the intranet penetration.
   ```

6. [SharpCheckInfo](https://github.com/uknowsec/SharpCheckInfo) (Get multiple host information)

   ```
   Collect target host information, including recently opened files, system environment variables and recycle bin files, etc.
   ```

7. [SharpSQLDump](https://github.com/uknowsec/SharpSQLDump) (Quickly list database data)

   ```
   Quickly obtain all database names, table names, and column names in the database during intranet penetration. Go through the data after specific judgments to save time. Applicable to mysql, mssql.
   ```

8. [SharpClipHistory](https://github.com/FSecureLABS/SharpClipHistory) (Get win10 clipboard)

   ```
   It can be used to read the contents of the user's clipboard history in Windows 10 starting from the 1809 Build version.
   ```

9. [SharpAVKB](https://github.com/uknowsec/SharpAVKB) (Comparison of anti-virus and patch)

   ```
   Windows anti-software comparison and patch number comparison.
   ```

10. [SharpEDRChecker](https://github.com/PwnDexter/SharpEDRChecker)(Get EDR information)

    ```
    Check the running process, process metadata, Dll loaded into the current process and each DLL metadata, public installation directory, installed services and binary metadata for each service, installed drivers and each driver Metadata, all of which exist for known defensive products such as AV, EDR, and logging tools.
    ```

11. [SharpDir](https://github.com/jnqpblc/SharpDir)(file search)

    ```
    Can search for files in local and remote file systems.
    ```

12. [Everything](https://www.voidtools.com/zh-cn/)(Establish http service file search)

## Positioning domain management

1. [PsLoggedon](https://docs.microsoft.com/zh-cn/sysinternals/downloads/psloggedon)

   ```
   Microsoft official tool.
   ```

2. [PVEFindADUser](https://github.com/chrisdee/Tools/tree/master/AD/ADFindUsersLoggedOn)

   ```
   It can be used to find the login location of Active Directory users and/or find who is logged in on a specific computer. This should include local users, users logged in through RDP, user accounts used to run services and scheduled tasks (only when the task is running at the time)
   ```

3. [netview](https://github.com/mubix/netview)

   ```
   Netview is an enumeration tool. It uses (with -d) the current domain or the specified domain (with -d) to enumerate hosts. If you want to specify a file containing a list of hosts, you can also use -f. Any hostname you wish to exclude can be specified in the list with -e. If you want to query domain groups and highlight the login locations of these users, use -g to specify the group.
   ```

## Read password

1. logonpasswords

2. Krbtgt hash

3. Detect wifi password

   -Get connected wifi

   -Get wifi password

   -[SharpWifiGrabber](https://github.com/r3nhat/SharpWifiGrabber)(Retrieve Wi-Fi password)

     ```
     Sharp Wifi Password Grabber retrieves Wi-Fi passwords in clear text from all WLAN configuration files saved on the workstation.
     ```

4. Modify the registry dump plaintext password

   -Show plaintext
   -Force screen lock
   -Hide plaintext

5. Extract browser data and password

   -[BrowserGhost](https://github.com/QAX-A-Team/BrowserGhost) (Extract browser password)

     ```
     Produced by Qi Anxin. This is a tool to grab browser passwords, more features will be added later
     ```

   -[SharpChromium](https://github.com/djhohnstein/SharpChromium) (Extract browser data)

     ```
     Used to retrieve Chromium data, such as cookies, history and saved login names.
     ```

   -[SharpWeb](https://github.com/djhohnstein/SharpWeb) (Extract browser data)

     ```
     The saved browser credentials can be retrieved from Google Chrome, Mozilla Firefox and Microsoft Internet Explorer/Edge.
     ```

6. Local program file password decryption
   -[SharpCloud](https://github.com/chrismaddalena/SharpCloud)(Get cloud credentials)

     ```
     Used to check if there are credential files related to AWS, Microsoft Azure and Google Compute.
     ```

   -[SharpDecryptPwd](https://github.com/uknowsec/SharpDecryptPwd)(from uknowsec)

     ```
     Analyze some programs whose passwords have been saved on the Windows system, including: Navicat, TeamViewer, FileZilla, WinSCP, Xmangager series products (Xshell, Xftp).
     ```

   -[SharpDecryptPwd](https://github.com/RcoIl/SharpDecryptPwd)(from RcoIl)

     ```
     This program is mainly 
