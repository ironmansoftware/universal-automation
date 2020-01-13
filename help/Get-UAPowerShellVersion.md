---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Get-UAPowerShellVersion

## SYNOPSIS
Returns PowerShell versions registered with UA.

## SYNTAX

### All (Default)
```
Get-UAPowerShellVersion [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Id
```
Get-UAPowerShellVersion [-Id] <Int64> [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Returns PowerShell versions registered with UA.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-UAPowerShellVersion
```

Returns all PowerShell versions registered with UA.

### Example 2
```powershell
PS C:\> Get-UAPowerShellVersion -Id 13
```

Returns PowerShell version with the ID 13.

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

### -Id
The ID of the PowerShell version to return.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
