---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Grant-UAAppToken

## SYNOPSIS
Grants app tokens for identities. 

## SYNTAX

### Grant
```
Grant-UAAppToken -Identity <Identity> [-Expiry <DateTime>] [-Role <String>] [-Audience <String>]
 [-Issuer <String>] [-SigningKey <String>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Generate
```
Grant-UAAppToken -IdentityName <String> [-Expiry <DateTime>] [-Role <String>] [-Audience <String>]
 [-Issuer <String>] [-SigningKey <String>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Grants app tokens for identities. Administrators can grant app tokens for any other user. Other users can grant app tokens for themselves. 

## EXAMPLES

### Example 1
```powershell
PS C:\> Grant-UAAppToken -Identity 12
```

Grants an app token for identity 12. 

### Example 2
```powershell
PS C:\> $Identity = Get-UAIdentity -Name 'Adam'
PS C:\> Grant-UAAppToken -Identity $Identity
```

Grants a new app token for the identity 'Adam'

### Example 3
```powershell
PS C:\> $Identity = Get-UAIdentity -Name 'Adam'
PS C:\> Grant-UAAppToken -Identity $Identity -Expiry ([DateTime]::Now.AddDays(12))
```

Grants a new app token for the identity 'Adam' that expires in 12 days. 

### Example 4
```powershell
PS C:\> $Identity = Get-UAIdentity -Name 'Adam'
PS C:\> Grant-UAAppToken -Identity $Identity -SigningKey ')()SDOK#w(*AY)'
```

Grants a new app token for the identity 'Adam' that uses a custom signing key. This signing key must match the one provided to Start-UAServer. 

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

### -Audience
The audience parameter for the JSON web token. 

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

### -Expiry
The expiration date of the app token. 

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The identity to grant the app token to. Use Get-UAIdentity to get an identity object. 

```yaml
Type: Identity
Parameter Sets: Grant
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityName
The name of the identity to grant the app token to. 

```yaml
Type: String
Parameter Sets: Generate
Aliases: UserName, Application

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Issuer
The issuer parameter of the JSON web token. 

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

### -Role
The role to assign to the identity of the app token. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Reader, Operator, Administrator

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SigningKey
The custom signing key for the JSON web token. This needs to match what is specified in Start-UAServer. 

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
