---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Get-UAJob

## SYNOPSIS
Returns jobs run within UA.

## SYNTAX

### All (Default)
```
Get-UAJob [-Tree] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Id
```
Get-UAJob [-Id] <Int64> [-Tree] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Identity
```
Get-UAJob [-Identity] <Identity> [-Tree] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Script
```
Get-UAJob [-Script] <Script> [-Tree] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Returns jobs run within UA. 

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-UAJob 
```

Returns all jobs run in UA. 

### Example 2
```powershell
PS C:\> Get-UAJob -Id 10
```

Returns job 10 from UA.

### Example 3
```powershell
PS C:\> $Script = Get-UAScript -Id 4
PS C:\> Get-UAJob -Script $Script
```

Returns all jobs run for script with Id 4. 

### Example 4
```powershell
PS C:\> Get-UAJob -Id 10 -Tree
```

Returns job 10 and any jobs (parent\child jobs) associated with it. 

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
The ID of the job to return.

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
Returns jobs run by this identity.

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

### -Script
Returns jobs based on this script. 

```yaml
Type: Script
Parameter Sets: Script
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tree
Returns all associated jobs of the specified script. 

```yaml
Type: SwitchParameter
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

### UniversalAutomation.Identity

### UniversalAutomation.Script

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
