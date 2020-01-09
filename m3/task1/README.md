```
_______________________________________________________________________________________
1
PS C:\Users\јлександра\ep> Get-Command | Where-Object {$_.CommandType -eq "Cmdlet"}
_______________________________________________________________________________________
2
md rd 
cd rd
Get-Process >> file.txt
md folder1
cd folder1
Get-Host >> file.txt 
Get-Help >> file.xml
md sub1
cd sub1
Get-Process >> file.txt
Get-Content file.txt >> file.xml
md  sub2
cd  sub2
Get-Process >> file.txt
Get-Process >> file.xml
cd /
_______________________________________________________________________________________
3
PS C:\> Get-Content C:\Users\јлександра\ep\rd\folder1\sub1\file.txt

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    618      19    25732      26792       0,44   1696   1 ApplicationFrameHost
    203       6     1740       3196              1352   1 atieclxx
    119       4      752        956              1324   0 atiesrxx
    159       6     1436       2772       0,06   4336   1 browser_broker
    490      17    19320      31692       0,47   5772   1 Calculator
    240       7     3156       6448       6,30   4696   1 conhost
    307       7     1008       1860               472   0 csrss
    356      10     1332       2332               596   1 csrss
    380       8     2672       6436       0,80   3640   1 ctfmon
    118       4     1020       5756       0,03    892   1 dllhost
    200       9     3160       6128       0,19   4520   1 dllhost
    671      24    25976      32692              1028   1 dwm
   2646      67    57656      83136      13,75   3696   1 explorer
     45       3     1408       1492               820   0 fontdrvhost
     45       4     1708       2696               828   1 fontdrvhost
    140       5     1300        216               416   0 GoogleCrashHandler
    192       7     1940        144              3532   0 GoogleUpdate
      0       0       36          4                 0   0 Idle
    856      12     3004       6400               652   0 lsass
      0       0      296      30440              1380   0 Memory Compression
    642      23   172208     149932       3,02   3228   1 Microsoft.Photos
    861      29    23288      15436       0,64   3500   1 MicrosoftEdge
    503      12     5544       3796       0,16   4976   1 MicrosoftEdgeCP
    397      10     4980       3296       0,11   5008   1 MicrosoftEdgeCP
    689      37   114988      82156              1016   0 MsMpEng
    423      18    16556      31452       0,28   3768   1 Music.UI
    185      20     4316       7632              5856   0 NisSrv
    756      17    45780      46352       8,08   5468   1 powershell
      0       4      892      10904                88   0 Registry
    383       9     3884       4304       0,13   6080   1 RtkNGUI
    232       7     2268      11860       0,31   2808   1 RuntimeBroker
    107       4      964       5500       0,05   3088   1 RuntimeBroker
    246       7     2608       5544       0,16   3476   1 RuntimeBroker
    434      12     5472      13088       1,61   3688   1 RuntimeBroker
    369       9     3564      13168       2,88   4628   1 RuntimeBroker
    139       4     1360       2796       0,11   4864   1 RuntimeBroker
    135       4     1620       7596       0,02   5444   1 RuntimeBroker
    103       4      920       2152       0,03   5952   1 RuntimeBroker
    678      26    17424       9224              5420   0 SearchIndexer
   1070      41    70348      97616       5,73   2792   1 SearchUI
    175       6     1768       6132              1244   0 SecurityHealthService
    224       7     2964      11416              3812   0 sedsvc
    302       6     2524       4360               644   0 services
    429      10     4288       1232       2,25   4732   1 SettingSyncHost
    726      21    33588      42988       2,13   4072   1 ShellExperienceHost
    603       9     4252      13008       2,61   3316   1 sihost
    175       5     1608        144       0,02   4280   1 SkypeBackgroundHost
     52       2      308        360               312   0 smss
    415      13     3908       4952              1936   0 spoolsv
    497      11     6360      14748               712   0 svchost
    922      13     6428      12352               836   0 svchost
    875       9     3828       6600               936   0 svchost
   1822      40    22660      34544              1096   0 svchost
    591      15    28816      32964              1144   0 svchost
    651      11    12528      15820              1420   0 svchost
    669      21     6664      12144              1428   0 svchost
    161       5     1448       3368              1488   0 svchost
    165       5     3068       7816              1520   0 svchost
    552      18     4628       8924              1584   0 svchost
    179       6     1532       2932              1728   0 svchost
    360       7     2644       7292              1736   0 svchost
    117       6     1132       1840              1832   0 svchost
    292       8     1524       3288              1840   0 svchost
    639      29    11328      14820              1976   0 svchost
    356      14     2552       3796              2080   0 svchost
    189       7     1536       6356              2708   0 svchost
    493      13     5752      17200       2,27   3388   1 svchost
   2352       0       56          8                 4   0 System
    751      24    20544      39944       0,75   1464   1 SystemSettings
    322      17     4680       9492       0,83   3460   1 taskhostw
    616      20    19576      13560       0,48   4120   1 Video.UI
    149       6      960       1448               576   0 wininit

_______________________________________________________________________________________
4
PS C:\Users\јлександра\ep> tree rd
—труктура папок
—ерийный номер тома: C8E3-0E32
C:\USERS\јЋ≈ —јЌƒ–ј\EP\RD
L---folder1
    L---sub1
        L---sub2
_______________________________________________________________________________________
5
PS C:\Users\јлександра\ep> Get-ChildItem rd/* -Include *.xml -Recurse


     аталог: C:\Users\јлександра\ep\rd\folder1\sub1\sub2


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----       26.12.2019      4:19          18406 file.xml


     аталог: C:\Users\јлександра\ep\rd\folder1\sub1


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----       26.12.2019      4:17          18406 file.xml


     аталог: C:\Users\јлександра\ep\rd\folder1


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----       26.12.2019      4:14           8300 file.xml
_______________________________________________________________________________________
6
PS C:\Users\јлександра\ep> Remove-Item .\rd\folder1\sub1\sub2\

ѕодтверждение
Ёлемент в C:\Users\јлександра\ep\rd\folder1\sub1\sub2\ имеет дочерние объекты, 
и параметр Recurse не указан. ѕри продолжении все дочерние объекты будут удалены 
вместе с элементом. ¬ы действительно хотите продолжить?
[Y] ƒа - Y  [A] ƒа дл€ всех - A  [N] Ќет - N  [L] Ќет дл€ всех - L  
[S] ѕриостановить - S  [?] —правка
(значением по умолчанию €вл€етс€ "Y"):y
_______________________________________________________________________________________
7
Get-Service | Where-Object {$_.status -eq "<status>"}
_______________________________________________________________________________________
8.1
PS C:\Users\јлександра\ep> Get-Process System

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
   2291       0       64         60                 4   0 System

_______________________________________________________________________________________
8.2
PS C:\Users\јлександра\ep> Get-Process -Id 4

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
   2312       0       64         60                 4   0 System
_______________________________________________________________________________________
8.3
PS C:\Users\јлександра\ep> $maybeobj =Get-Process
PS C:\Users\јлександра\ep> Get-Process -InputObject  $maybeobj
```