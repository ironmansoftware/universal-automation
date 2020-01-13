---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# New-UACredential

## SYNOPSIS
Creates a new credential to be used for running scripts as the specified user. 

## SYNTAX

```
New-UACredential [-UserName] <String> [-Password] <Variable> [-ComputerName <String>] [-AppToken <String>]
 [<CommonParameters>]
```

## DESCRIPTION
Creates a new credential to be used for running scripts as the specified user. This can be used with Invoke-UAScript and New-UASchedule to run a script as a different user. 

## EXAMPLES

### Example 1
```powershell
PS C:\> $Variable = Get-UAVariable -Name 'password' 
PS C:\> $Credential = New-UACredential -UserName 'adam' -Password $Variable 
```

Retrieves the password variable and creates a new credential for the user 'adam'. The credential must be a secret coming from a secret manager. 

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

### -Password
The password variable to use for the password value of this credential. Use Get-UAVariable to retrieve a secret variable. The variable must be managed by a secret manager. 

```yaml
Type: Variable
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
The username of the credential. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
