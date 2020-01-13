---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Set-UAScript

## SYNOPSIS
Sets properties of a script. 

## SYNTAX

### Id
```
Set-UAScript [-Id] <Int64> [-Name <String>] [-Description <String>] [-ManualTime <Double>] [-Status <String>]
 [-Content <String>] [-Notes <String>] [-RequiredPowerShellVersion <String>] [-ComputerName <String>]
 [-AppToken <String>] [<CommonParameters>]
```

### Script
```
Set-UAScript [-Script] <Script> [-Name <String>] [-Description <String>] [-ManualTime <Double>]
 [-Status <String>] [-Content <String>] [-Notes <String>] [-RequiredPowerShellVersion <String>]
 [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### ScriptBlock
```
Set-UAScript [-Name <String>] [-Description <String>] [-ManualTime <Double>] [-Status <String>]
 [-Content <String>] [-ScriptBlock <ScriptBlock>] [-Notes <String>] [-RequiredPowerShellVersion <String>]
 [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Sets properties of a script. Properties will be stored in both the database and the git repo. 

## EXAMPLES

### Example 1
```powershell
PS C:\> $Script = Get-UAScript -Name 'Script1.ps1'
PS C:\> Set-UAScript -Script $Script -Description 'My favorite script' -ManualTime 123
```

Sets the description and manual time of Script1.ps1.

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

### -Content
The content of the script. 

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
The description of the script. 

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

### -Id
The ID of the script to set. 

```yaml
Type: Int64
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManualTime
The manual execution time of this script. 

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of this script. 

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

### -Notes
Notes to include with this script. 

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

### -RequiredPowerShellVersion
The required PowerShell version for this script. Use Get-UAPowerShellVersion to retrieve a PowerShellVersion object.

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

### -Script
The script to set properties on. Use Get-UAScript to retrieve a Script object. 

```yaml
Type: Script
Parameter Sets: Script
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScriptBlock
The script block used to set the content of the script. 

```yaml
Type: ScriptBlock
Parameter Sets: ScriptBlock
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
The status of the script. This is not currently used. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Draft, Pending Review, Pending, Review, Published, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### UniversalAutomation.Script

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
