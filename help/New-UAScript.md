---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# New-UAScript

## SYNOPSIS
Creates a new script within UA.

## SYNTAX

```
New-UAScript -ScriptBlock <ScriptBlock> [-ManualTime <Int32>] -Name <String> [-Description <String>]
 [-Parameter <ScriptParameter[]>] [-Tag <Tag[]>] [-Status <ScriptStatus>] [-Folder <Folder>]
 [-RequiredPowerShellVersion <String>] [-Notes <String>] [-ComputerName <String>] [-AppToken <String>]
 [<CommonParameters>]
```

## DESCRIPTION
Creates a new script within UA. The script will be committed to the local git repository as well as an optionally configured remote. 

## EXAMPLES

### Example 1
```powershell
PS C:\> New-UAScript -ScriptBlock { Get-Process } -Name 'Get running processes'
```

Creates the script "Get running processes" in UA. A script named 'Get running processes.ps1" will be created in the Git repoisitory. 

### Example 2
```powershell
PS C:\> New-UAScript -ScriptBlock { param($Value) Invoke-WebRequest http://myserver.com -Body $Value } -Name 'InvokeMyServer'
```

Creates the script "InvokeMyServer" in UA. A script named 'InvokeMyServer.ps1" will be created in the Git repoisitory. This script will accept the parameter Value which will be a textbox in the UA UI. 

### Example 3
```powershell
PS C:\> $Folder = Get-UAFolder -Name 'Scripts'
PS C:\> New-UAScript -ScriptBlock { Get-Process } -Name 'GetProcess' -Folder Scripts
```

Creates the script "GetProcess" in UA. A script named 'GetProcess.ps1" will be created in the Git repoisitory. This script will be created within the Scripts folder. 

### Example 4
```powershell
PS C:\> $PSVersion = Get-UAPowerShellVersion -Name 'PS7'
PS C:\> New-UAScript -ScriptBlock { Get-Process } -Name 'GetProcess' -PowerShellVersion $PSVersion
```

Creates the script "GetProcess" in UA. A script named 'GetProcess.ps1" will be created in the Git repoisitory. This script will be run using the PS7 PowerShell version. 

## PARAMETERS

### -AppToken
An app token to access the UA API. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
The HTTP address of the UA REST API server.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A description for the script. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Folder
The folder to create the script in. Use Get-UAFolder to get a Folder object. 

```yaml
Type: Folder
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManualTime
The number of seconds in manual time this particular action would take if taken be a person. This is used for calculating the time saved. 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the script. PS1 will be appended to the file on disk if it's not included. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Notes
Any notes to include with this script. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
Manually defined parameters for this script. Parameters will automatically be generated when using a param block in the ScriptBlock. 

```yaml
Type: ScriptParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequiredPowerShellVersion
Specifies a required PowerShell version to use when running scripts. You can use the Get-UAPowerShellVersion cmdlet to get a required PowerShell version. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
A script block to execute when running this script. 

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
The status of this script. This current isn't used. 

```yaml
Type: ScriptStatus
Parameter Sets: (All)
Aliases:
Accepted values: Draft, Pending_Review, Published, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Any tags to assign to this script. Use Get-UATag to get tag objects. 

```yaml
Type: Tag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
