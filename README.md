### 硬件配置:
| 类型     | 配置                             |
| -------- | -------------------------------- |
| CPU      | I5-8400                          |
| 主板     | 戴尔030VXY-Q370芯片组            |
| 显卡     | Intel UHD Graphics 630           |
| 网卡     | Intel Ethernet Connection I219-V |
| 声卡     | ALC-255                          |
| 无线网卡 | BCM-94352Z NGFF M2               |

### bios设置：

1. General - Advanced Boot Options 取消勾选 Enable Legacy Option ROMs
2. System Configuration - SATA Operation 选择 AHCI
3. System Configuration - Serial Port 选择 Disabled
4. Video - Primary Display 选择 Intel HD Graphics
5. Secure Boot - Secure Boot Enable 取消勾选 Secure Boot Enable
6. Intel Software Guard Extensions - Intel SGX Enable 选择 Disabled
7. Virtualization Support - Virtualization 勾选 Enable Intel Virtualization Technology
8. Virtualization Support - VT for Direct I/O 取消勾选 Enable VT for Direct I/O

### 修改 DVMT：
1. 在引导页按空格，选modGRUBShell，输入
   ```
   setup_var 0x8DC 0x2
   ```
2. 按回车之后，dvmt修改为64mb

3. 如果是1080p这样的显示器，不修改dvmt(最好都修改)可尝试用另一个config，如果是2k以上的显示器，一定要改dvmt,否则进不去。