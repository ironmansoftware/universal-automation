---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Set-UAVariable

## SYNOPSIS
Sets the properties of a variable. 

## SYNTAX

### Id
```
Set-UAVariable [-Id] <Int64> [-Value <String>] [-Name <String>] [-ComputerName <String>] [-AppToken <String>]
 [<CommonParameters>]
```

### Variable
```
Set-UAVariable [-Variable] <Variable> [-Value <String>] [-Name <String>] [-ComputerName <String>]
 [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Sets the properties of a variable. 

## EXAMPLES

### Example 1
```powershell
PS C:\> $Variable = Get-UAVariable -Name 'username'
PS C:\> Set-UAVariable -Variable $Variable -Value 'lee'
```

Sets the value of the username variable to lee. 

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
The ID of the variable to set. 

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

### -Name
The name of the variable. 

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

### -Value
The value of the variable. 

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

### -Variable
The variable to set. Use Get-UAVariable to retrieve a Variable object.  

```yaml
Type: Variable
Parameter Sets: Variable
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

### UniversalAutomation.Variable

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
