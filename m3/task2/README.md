```
1
Get-Service | Format-Wide -Column 4 | Format-Table Width=1024 >> file_1024_TAB.txt
_____________________________________________________________________________________
2.1
$arr = New-Object 'object[,]' 3,3
PS C:\Users\Александра\ep\task2> $arr[0,0] = 1
 PS C:\Users\Александра\ep\task2> $arr[0,1] = 1
  PS C:\Users\Александра\ep\task2> $arr[0,2] = 1
   PS C:\Users\Александра\ep\task2> $arr[1,0] = 2
    PS C:\Users\Александра\ep\task2> $arr[1,1] = 2
     PS C:\Users\Александра\ep\task2> $arr[1,2] = 2
      PS C:\Users\Александра\ep\task2> $arr[2,0] = 3
       PS C:\Users\Александра\ep\task2> $arr[2,1] = 3
        PS C:\Users\Александра\ep\task2> $arr[2,2] = 3
         PS C:\Users\Александра\ep\task2>
	  >> Write-Host $arr[0,0] $arr[0,1] $arr[0,2]
	  >> Write-Host $arr[1,0] $arr[1,1] $arr[1,2]
	  >> Write-Host $arr[2,0] $arr[2,1] $arr[2,2]
	    1 1 1
            2 2 2
	    3 3 3
2.2
PS C:\Users\Александра\ep\task2> $arr[1,1] = 4
 PS C:\Users\Александра\ep\task2>
   >> Write-Host $arr[0,0] $arr[0,1] $arr[0,2]
   >> Write-Host $arr[1,0] $arr[1,1] $arr[1,2]
   >> Write-Host $arr[2,0] $arr[2,1] $arr[2,2]
    1 1 1
    2 4 2
    3 3 3
_____________________________________________________________________________________
3
PS C:\Users\Александра\ep\task2>
>> Write-Host "\/"
>> $user_says = Read-Host
>> (Get-Host).UI.RawUI.ForegroundColor="Yellow"
>> (Get-Host).UI.RawUI.BackgroundColor="Gray"
>> Write-Host $user_says "-сказал пользователь"
_____________________________________________________________________________________
6
PS C:\Users\Александра>
>> for($tpi = 0 ; $tpi -le 16; $tpi++){
>> $temp = $tpi % 2
>> if($temp -eq 0){
>> Write-Host $tpi
>> }
>> }
_____________________________________________________________________________________
7
PS C:\Users\Александра>
>> for($tpi = 0 ; $tpi -le 5; $tpi++){
>> Write-Host > $tpi".txt"
>> }
>> for($tpi = 0 ; $tpi -le 5; $tpi++){
>> $str = "log_$tpi.txt"
>> Write-Host > $str
>> }
_____________________________________________________________________________________
8
$var = Get-ChildItem .\Public\ -Recurse -Directory
$ls = Get-ChildItem .\Public\ -Directory
$sdir_count = $var.Length - $ls.Length
$names = $ls.Name
Write-Host "В моём домашнем каталоге > $sdir_count поддиректорий ($names)"
_____________________________________________________________________________________
9
PS C:\Users>
>> Write-Host "Enter WORD \/"
>> $str = Read-Host
>> $char_count = $str.Length
>> Write-Host "Chrars >$char_count"
_____________________________________________________________________________________ 
10
>> Write-Host "Set A,B and C arg \/"
>> [int]$a_arg = Read-Host
>> [int]$b_arg = Read-Host
>> [int]$c_arg = Read-Host
>> $res = ($a_arg + $b_arg)/$c_arg
>> Write-Host "Res (a+b)/c =" $res
_____________________________________________________________________________________ 
11
>> Write-Host "Set ARG(1) and ARG(2)"
>> Try {
>> [int]$f_arg = Read-Host
>> [int]$s_arg = Read-Host
>> if($f_arg -gt $s_arg){
>> $temp = $f_arg
>> }
>> else{
>> $temp = $s_arg
>> }
>>  Write-Host "Res > Arg($temp)"
>> }
>> catch {
>> Write-Host "You Entered Invalid Argument"
>> }
>> Finally {
>> Write-Host "end"
>> }
_____________________________________________________________________________________
12
>> $get_day = (Get-Date).ToString('dd')
>> $files_update = Get-ChildItem $dir_path -Include *.* -Recurse
>> for($j = 0 ; $j -le $files_update.Length;$j++){
>> $date_files[$j] = $files_update[$j].LastWriteTime.ToString('dd')
>> }
>> $time_to_die = $get_day - $date_files
>> if($time_to_die -gt 7){
>> For($i = 0; $i -le $files_update.Length;$i++){
>> if($date_files[$i] -gt 7){
>> Get-ChildItem $dir_path -Recurse | Remove-Item $files_update[$i].Name
>> }
>> }
>> }
```