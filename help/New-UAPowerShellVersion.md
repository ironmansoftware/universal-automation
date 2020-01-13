---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# New-UAPowerShellVersion

## SYNOPSIS
Creates a new PowerShell version within UA.

## SYNTAX

```
New-UAPowerShellVersion -Version <String> -Path <String> [-Arguments <String[]>] [-ComputerName <String>]
 [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new PowerShell version within UA. PowerShell versions are used to registering PowerShell runtimes with UA. When UA first starts, it will attempt to locate PowerShell versions available on disk and autopopulate the database with those versions and paths. This cmdlet allows you to add new versions that were not automatically detected. 

## EXAMPLES

### Example 1
```powershell
PS C:\> New-UAPowerShellVersion -Version 'PowerShell7' -Path 'C:\Program Files\PowerShell\7\Pwsh.exe'
```

Creates a new PowerShell version for PowerShell version 7.

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

### -Arguments
Arguments to pass to the PowerShell process when starting a new job. 

```yaml
Type: String[]
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

### -Path
The path on disk to the PowerShell executable. 

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

### -Version
A name for this version. 

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
