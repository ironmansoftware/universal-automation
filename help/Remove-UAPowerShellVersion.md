---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Remove-UAPowerShellVersion

## SYNOPSIS
Removes a PowerShel Version from UA. 

## SYNTAX

```
Remove-UAPowerShellVersion [-PowerShellVersion] <PowerShellVersion> [-ComputerName <String>]
 [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Removes a PowerShell version from UA.

## EXAMPLES

### Example 1
```powershell
PS C:\> $PSVersion = Get-UAPowerShellVersion -Id 12
PS C:\> Remove-UAPowerShellVersion -PowerShellVersion $PSVersion
```

Removes PowerShell version 12. 

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

### -PowerShellVersion
The PowerShell Version to remove. Use Get-UAPowerShellVersion to retrieve a PowerShell Version object.

```yaml
Type: PowerShellVersion
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
