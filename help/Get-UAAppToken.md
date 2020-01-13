---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Get-UAAppToken

## SYNOPSIS

Returns app tokens stored in the UA database. 

## SYNTAX

### All (Default)
```
Get-UAAppToken [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Id
```
Get-UAAppToken [-Id] <Int64> [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Identity
```
Get-UAAppToken [-Identity] <Identity> [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION

Gets app tokens stored in the UA database. 

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-UAAppToken 
```

Returns all app tokens.

### Example 2
```powershell
PS C:\> Get-UAAppToken -Id 123
```

Returns the token by ID 123

### Example 3
```powershell
PS C:\> $Identity = Get-UAIdentity -Name 'adam'
PS C:\> Get-UAAppToken -Identity $Identity
```

Returns app tokens assigned to the identity 'adam'

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
The ID of the app token to retrieve. 

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

### -Identity
The identity to retrieve app tokens for. Use a value returned from Get-UAIdentity or New-UAIdentity to pass to this parameter. 

```yaml
Type: Identity
Parameter Sets: Identity
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

### UniversalAutomation.Identity

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
