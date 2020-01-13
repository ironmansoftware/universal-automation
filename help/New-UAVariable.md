---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# New-UAVariable

## SYNOPSIS
Creates a new variable in UA.

## SYNTAX

### Public
```
New-UAVariable -Name <String> [-Value <String>] [-ComputerName <String>] [-AppToken <String>]
 [<CommonParameters>]
```

### Secret
```
New-UAVariable -Name <String> [-Value <String>] -SecretManager <SecretManager> [-ComputerName <String>]
 [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new variable in UA. Variables are available in all scripts that run within UA. 

## EXAMPLES

### Example 1
```powershell
PS C:\> New-UAVariable -Name 'UserName' -Value 'Adam'
```

Creates a new variable in UA named `UserName`. You can use the $UserName variable in all your scripts. 

### Example 2
```powershell
PS C:\> $SecretManager = Get-UASecretManager -Name 'Vault'
PS C:\> New-UAVariable -Name 'UserName' -Value 'Adam' -SecretManager $SecretManager
```

Creates a new variable in the secert manager `Vault`. The variable's value is not stored in UA and will only be retrieved when running scripts. 

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

### -Name
The name of the variable. You can reference this in your scripts just as you would with other variables. 

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

### -SecretManager
The secert manager to store the variable value in. Use Get-UASecretManager to get a SecertManager object. 

```yaml
Type: SecretManager
Parameter Sets: Secret
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
