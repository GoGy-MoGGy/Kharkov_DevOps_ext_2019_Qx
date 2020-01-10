```
_______________________________________________________________________________________
1
systeminfo
_______________________________________________________________________________________
2
gcim win32_startupcommand
_______________________________________________________________________________________
3
Get-WmiObject -Class Win32_NetworkAdapterConfiguration
_______________________________________________________________________________________
4


DHCPEnabled      : True
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : kdnic
Description      : Microsoft Kernel Debug Network Adapter
Index            : 0

DHCPEnabled      : True
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : rt640x86
Description      : Realtek PCIe GBE Family Controller
Index            : 1

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : RasSstp
Description      : WAN Miniport (SSTP)
Index            : 2

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : RasAgileVpn
Description      : WAN Miniport (IKEv2)
Index            : 3

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : Rasl2tp
Description      : WAN Miniport (L2TP)
Index            : 4

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : PptpMiniport
Description      : WAN Miniport (PPTP)
Index            : 5

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : RasPppoe
Description      : WAN Miniport (PPPOE)
Index            : 6

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : NdisWan
Description      : WAN Miniport (IP)
Index            : 7

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : NdisWan
Description      : WAN Miniport (IPv6)
Index            : 8

DHCPEnabled      : False
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : NdisWan
Description      : WAN Miniport (Network Monitor)
Index            : 9

DHCPEnabled      : True
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : usbrndis6
Description      : Remote NDIS based Internet Sharing Device
Index            : 10

DHCPEnabled      : True
IPAddress        :
DefaultIPGateway :
DNSDomain        :
ServiceName      : usbrndis6
Description      : Remote NDIS based Internet Sharing Device
Index            : 11
_______________________________________________________________________________________
5
ping www.google.com
При проверке связи не удалось обнаружить узел www.google.com.
Проверьте имя узла и повторите попытку.
_______________________________________________________________________________________
6
net share S_DIR=C:\Users\Александра\Documents\ /GRANT:Default,[READ] /USERS:7
_______________________________________________________________________________________
8
$shell = New-Object -ComObject shell.application
$network = $shell.NameSpace("::{208D2C60-3AEA-1069-A2D7-08002B30309D}")
$network.Items()
$EntireNetwork = $network.Items().item("EntireNetwork").GetFolder
foreach ($item in $EntireNetwork.Items())
{
    if ($item.Name -match "Microsoft Windows Network")
    {
        $MSWinNetwork = $item.GetFolder
    }
}
foreach ($item in $MSWinNetwork.Items())
{
    $Domain = $item.GetFolder
    foreach ($DomainItem in $Domain.Items())
    {
        $Computer_name = $DomainItem.name
        //нужно было это отправить нп печать... но что-то пошло не так ....
        $Computer_name
    }
}
_______________________________________________________________________________________
```
