bios设置：

General - Advanced Boot Options 取消勾选 Enable Legacy Option ROMs

System Configuration - SATA Operation 选择 AHCI

System Configuration - Serial Port 选择 Disabled

Video - Primary Display 选择 Intel HD Graphics

Secure Boot - Secure Boot Enable 取消勾选 Secure Boot Enable

Intel Software Guard Extensions - Intel SGX Enable 选择 Disabled

Virtualization Support - Virtualization 勾选 Enable Intel Virtualization Technology

Virtualization Support - VT for Direct I/O 取消勾选 Enable VT for Direct I/O


修改 DVMT 为 64MB：
在引导页按空格，选modGRUBShell，输入

setup_var 0x8DC 0x2

按回车之后，dvmt修改为64mb

如果是1080p这样的显示器，不修改dvmt(最好都修改)可尝试用另一个config，如果是2k以上的显示器，一定要改dvmt,否则进不去。
