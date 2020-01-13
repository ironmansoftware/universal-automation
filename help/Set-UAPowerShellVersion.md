---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Set-UAPowerShellVersion

## SYNOPSIS
Sets properties of a PowerShell Version.

## SYNTAX

### Id
```
Set-UAPowerShellVersion [-Id] <Int64> [-Version <String>] [-Path <String>] [-Arguments <String[]>]
 [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### PowerShellVersion
```
Set-UAPowerShellVersion [-PowerShellVersion] <PowerShellVersion> [-Version <String>] [-Path <String>]
 [-Arguments <String[]>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Sets properties of a PowerShell Version.

## EXAMPLES

### Example 1
```powershell
PS C:\> Set-UAPowerShellVersion -Id 12 -Version 'PSv7.1'
```

Sets the version name of PowerShell Version 12 to 'PSv7.1'

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

### -Arguments
Arguments to use when starting the PowerShell host for this version.

```yaml
Type: String[]
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

### -Id
The ID of the PowerShell version to set. 

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

### -Path
The path of the PowerShell version. 

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

### -PowerShellVersion
The PowerShell version to set. Use Get-UAPowerShellVersion to retrieve a PowerShellVersion object. 

```yaml
Type: PowerShellVersion
Parameter Sets: PowerShellVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Version
The name of the version. 

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### UniversalAutomation.PowerShellVersion

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
