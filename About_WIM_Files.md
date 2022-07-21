### DISM Linux下的实现
```bash
apt install wimtools
```

|            命令                  |             用途                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------|
|wimlib-imagex                    |解压,创建,修改,或者挂载WIM归档文件（Extract, create, modify, or mount a WIM archive）          |
|wimcapture  wimappend            |捕获或者往WIM归档中追加文件（Capture or append a WIM image）                                  |              
|wimapply                         |同DISM Apply（Apply a WIM image）                                                          |
|wimdelete                        |从WIM归档文件中删除一个镜像(Delete an image from a WIM archive)                               |
|wimexport                         |从WIM归档文件中导出镜像(Export image(s) from a WIM archive)                                 |
|wimextract                        |解压WIM镜像中的文件(Extract files from a WIM image)                                        |
|wimdir                            |列出WIM镜像中包含的文件(List the files contained in a WIM image)                            |
|wiminfo                           |显示或修改关于WIM文件或镜像信息（Display or change information about a WIM file or image）    |
|wimjoin                           |把拆分的WIM合并入一个独立的WIM（Join a split WIM into a standalone WIM）                     |
|wimmount  wimmountrw  wimunmount  |挂载卸载WIM镜像(Mount or unmount a WIM image)                                             |
|wimoptimize                       |优化WIM归档（Optimize a WIM archive）                                                     |
|wimsplit                          |把一个WIM拆分成多份（Split a WIM archive into multiple parts）                              |
|wimverify                         |校验WIM归档（Verify a WIM archive）                                                       |


```bash
┌──(root😘🧔A51M)-[/tmp]
└─#mount en-us_windows_11_business_editions.iso /mnt
┌──(root😘🧔A51M)-[/tmp]
└─#cp /mnt/sources/install.wim .
┌──(root😘🧔A51M)-[/tmp]
└─#wiminfo install.wim 
WIM Information:
----------------
Path:           install.wim
GUID:           0x3558ffe27ad26047ab5699835b6b672f
Version:        68864
Image Count:    10
Compression:    LZX
Chunk Size:     32768 bytes
Part Number:    1/1
Boot Index:     0
Size:           4939845106 bytes
Attributes:     Relative path junction

Available Images:
-----------------
Index:                  1
Name:                   Windows 10 Education
Description:            Windows 10 Education
Display Name:           Windows 11 Education
Display Description:    Windows 11 Education
Directory Count:        28879
File Count:             111139
Total Bytes:            16467932106
Hard Link Bytes:        7141512848
Creation Time:          Wed Jun 29 07:11:06 2022 UTC
Last Modification Time: Wed Jun 29 07:36:06 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             Education
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  Education
WIMBoot compatible:     no

Index:                  2
Name:                   Windows 10 Education N
Description:            Windows 10 Education N
Display Name:           Windows 11 Education N
Display Description:    Windows 11 Education N
Directory Count:        27790
File Count:             104951
Total Bytes:            15768063705
Hard Link Bytes:        6859052950
Creation Time:          Wed Jun 29 07:12:59 2022 UTC
Last Modification Time: Wed Jun 29 07:36:35 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             EducationN
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  EducationN
WIMBoot compatible:     no

Index:                  3
Name:                   Windows 10 Enterprise
Description:            Windows 10 Enterprise
Display Name:           Windows 11 Enterprise
Display Description:    Windows 11 Enterprise
Directory Count:        28879
File Count:             111144
Total Bytes:            16468054121
Hard Link Bytes:        7141512848
Creation Time:          Wed Jun 29 07:24:40 2022 UTC
Last Modification Time: Wed Jun 29 07:37:02 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             Enterprise
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  Enterprise
WIMBoot compatible:     no

Index:                  4
Name:                   Windows 10 Enterprise N
Description:            Windows 10 Enterprise N
Display Name:           Windows 11 Enterprise N
Display Description:    Windows 11 Enterprise N
Directory Count:        27790
File Count:             104948
Total Bytes:            15767989170
Hard Link Bytes:        6859052950
Creation Time:          Wed Jun 29 07:05:09 2022 UTC
Last Modification Time: Wed Jun 29 07:37:27 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             EnterpriseN
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  EnterpriseN
WIMBoot compatible:     no

Index:                  5
Name:                   Windows 10 Pro
Description:            Windows 10 Pro
Display Name:           Windows 11 Pro
Display Description:    Windows 11 Pro
Directory Count:        28879
File Count:             111135
Total Bytes:            16465008286
Hard Link Bytes:        7141512848
Creation Time:          Wed Jun 29 07:00:14 2022 UTC
Last Modification Time: Wed Jun 29 07:37:55 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             Professional
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  Professional
WIMBoot compatible:     no

Index:                  6
Name:                   Windows 10 Pro N
Description:            Windows 10 Pro N
Display Name:           Windows 11 Pro N
Display Description:    Windows 11 Pro N
Directory Count:        27790
File Count:             104946
Total Bytes:            15765543280
Hard Link Bytes:        6859052950
Creation Time:          Wed Jun 29 06:59:53 2022 UTC
Last Modification Time: Wed Jun 29 07:38:21 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             ProfessionalN
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  ProfessionalN
WIMBoot compatible:     no

Index:                  7
Name:                   Windows 10 Pro Education
Description:            Windows 10 Pro Education
Display Name:           Windows 11 Pro Education
Display Description:    Windows 11 Pro Education
Directory Count:        28879
File Count:             111137
Total Bytes:            16467883316
Hard Link Bytes:        7141512848
Creation Time:          Wed Jun 29 07:05:42 2022 UTC
Last Modification Time: Wed Jun 29 07:38:47 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             ProfessionalEducation
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  ProfessionalEducation
WIMBoot compatible:     no

Index:                  8
Name:                   Windows 10 Pro Education N
Description:            Windows 10 Pro Education N
Display Name:           Windows 11 Pro Education N
Display Description:    Windows 11 Pro Education N
Directory Count:        27790
File Count:             104949
Total Bytes:            15768014015
Hard Link Bytes:        6859052950
Creation Time:          Wed Jun 29 07:07:47 2022 UTC
Last Modification Time: Wed Jun 29 07:39:12 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             ProfessionalEducationN
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  ProfessionalEducationN
WIMBoot compatible:     no

Index:                  9
Name:                   Windows 10 Pro for Workstations
Description:            Windows 10 Pro for Workstations
Display Name:           Windows 11 Pro for Workstations
Display Description:    Windows 11 Pro for Workstations
Directory Count:        28879
File Count:             111138
Total Bytes:            16467907711
Hard Link Bytes:        7141512848
Creation Time:          Wed Jun 29 07:08:24 2022 UTC
Last Modification Time: Wed Jun 29 07:39:39 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             ProfessionalWorkstation
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  ProfessionalWorkstation
WIMBoot compatible:     no

Index:                  10
Name:                   Windows 10 Pro N for Workstations
Description:            Windows 10 Pro N for Workstations
Display Name:           Windows 11 Pro N for Workstations
Display Description:    Windows 11 Pro N for Workstations
Directory Count:        27790
File Count:             104950
Total Bytes:            15768038860
Hard Link Bytes:        6859052950
Creation Time:          Wed Jun 29 07:10:22 2022 UTC
Last Modification Time: Wed Jun 29 07:40:03 2022 UTC
Architecture:           x86_64
Product Name:           Microsoft® Windows® Operating System
Edition ID:             ProfessionalWorkstationN
Installation Type:      Client
Product Type:           WinNT
Product Suite:          Terminal Server
Languages:              en-US 
Default Language:       en-US
System Root:            WINDOWS
Major Version:          10
Minor Version:          0
Build:                  22000
Service Pack Build:     795
Service Pack Level:     0
Flags:                  ProfessionalWorkstationN
WIMBoot compatible:     no
```
