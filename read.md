Function opop
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
	
	$segsd = [System.Convert]::FromBase64String($K)
		
	$werfg = (New-Object  Management.Automation.PSCredential ' ', ($obfString |ConvertTo-SecureString -Key  $segsd)).GetNetworkCredential().Password

	return $werfg
}
