---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Connect-UAServer

## SYNOPSIS

Connects to a UA server.

## SYNTAX

```
Connect-UAServer -ComputerName <String> [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Connects to a UA server. Additional commands will not need to specify the ComputerName or AppToken parameters. 

## EXAMPLES

### Example 1
```powershell
PS C:\> Connect-UDServer -ComputerName http://localhost:10000 -AppToken asdfa32faeshfoiahoiafhs
```

Connects to a local UA server on port 10000.

## PARAMETERS

### -AppToken
The app token for an authenticated UA server. 

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
The HTTP URL of the UA REST API.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
