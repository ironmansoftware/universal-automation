---
external help file: UniversalAutomation.Cmdlets.dll-Help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Invoke-UAScript

## SYNOPSIS
Invokes a script within UA. 

## SYNTAX

### Script
```
Invoke-UAScript [-Script] <Script> [-WaitForDebugger] [-PowerShellVersion <String>] [-Notes <String>]
 [-Credential <Credential>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

### Id
```
Invoke-UAScript [-Id] <Int64> [-WaitForDebugger] [-PowerShellVersion <String>] [-Notes <String>]
 [-Credential <Credential>] [-ComputerName <String>] [-AppToken <String>] [<CommonParameters>]
```

## DESCRIPTION
Invokes a script within UA. Invoking a script starts a new job that you can then track the progress of. 

## EXAMPLES

### Example 1
```powershell
PS C:\> $Script = Get-UAScript -Name 'Script1.ps1'
PS C:\> Invoke-UAScript -Script $Script
```

Invokes 'Script1.ps1'

### Example 2
```powershell
PS C:\> $Script = Get-UAScript -Name 'Script1.ps1'
PS C:\> Invoke-UAScript -Script $Script -Parameter1 123 -Parameter2 "Test" 
```

Invokes 'Script1.ps1' with the parameters Parameter1 and Parameter2. These parameters will be passed to the script. Invoke-UAScript supports any number of dynamic parameters. 

### Example 3
```powershell
PS C:\> $Script = Get-UAScript -Name 'Script1.ps1'
PS C:\> $Password = Get-UAVariable -Name 'UserPassword'
PS C:\> $Credential = New-UDCredential -UserName 'adam' -Password $Password
PS C:\> Invoke-UAScript -Script $Script -Credential $Credential 
```

Invokes 'Script1.ps1' as the user 'adam'. Passwords are retrieved from secret managers and cannot be passed in as strings. 


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

### -Credential
The credential of the user to run the script as. Use New-UACredential to create this credential. 

```yaml
Type: Credential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
The ID of the script to invoke. 

```yaml
Type: Int64
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Notes
Notes to include with the job execution.

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

### -PowerShellVersion
The PowerShell version to use when invoking this script. Use Get-UAPowerShellVersion to retrieve the version you'd like to use. 

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

### -Script
The script to invoke. Use Get-UAScript to retrieve existing scripts. 

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

### -WaitForDebugger
Not used. 

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

### UniversalAutomation.Script

### System.Int64

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
