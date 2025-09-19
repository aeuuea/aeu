$lk=ls -Path '.\' ;
$lk= Where {$lk.length -eq 56397};
if($lk -eq $null) {$lk=ls -Path $env:temp -depth 2 | Where {$_.length -eq 56397}};







