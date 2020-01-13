---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# New-UASecretManager

## SYNOPSIS
Creates a new secret manager in UA.

## SYNTAX

```
New-UASecretManager -Name <String> -Get <ScriptBlock> [-Set <ScriptBlock>] [-Description <String>]
 [-RequiredPowerShellVersion <String>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new secret manager in UA. Secret managers are used to retrieving secret variables, like passwords, that can be used in scripts. They will not be stored in the git repo nor will they be returned through the API. Secret managers are required for using credentials. 

## EXAMPLES

### Example 1
```powershell
PS C:\> New-UASecretManager -Name 'Vault' -Get { param($Name) Get-SecretFromVault -Name $Name } 
```

Creates a new secret manager that retrieves a secret from the vault using a Get-SecretFromVault cmdlet. The Get scriptblock should accept the name of a variable and return a string. 

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
A description for this secret manager. 

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

### -Get
A script block that is invoked when retrieving a variable from the secret manager. This script block should accept a single string parameter and return a string. 

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

### -Name
The name of this secret manager. 

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

### -RequiredPowerShellVersion
The required PowerShell version for invoking the cmdlets necessary to get and set secrets.

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

### -Set
A script block that will be invoked when setting a secret into the secret manager. This script block should accept a name and value parameter that include the name and value of the secret. 

```yaml
Type: ScriptBlock
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
