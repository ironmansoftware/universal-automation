---
external help file: UniversalAutomation-help.xml
Module Name: UniversalAutomation
online version:
schema: 2.0.0
---

# Start-UAServer

## SYNOPSIS
Starts the UA server. 

## SYNTAX

```
Start-UAServer [[-Port] <String>] [[-ConnectionString] <String>] [[-GitRemote] <String>]
 [[-GitRemoteCredential] <PSCredential>] [[-JwtSigningKey] <String>] [[-JwtAudience] <String>]
 [[-JwtIssuer] <String>] [[-LocalComputerName] <String>] [[-CertificateFile] <String>]
 [[-CertificatePassword] <SecureString>] [-InProcess] [<CommonParameters>]
```

## DESCRIPTION
Starts the UA server. 

## EXAMPLES

### Example 1
```powershell
PS C:\> Start-UAServer -Port 1000
```

### Example 2
```powershell
PS C:\> Start-UAServer -Port 1000 -CertificateFile cert.pfx -CertificatePassword password134
```

Starts the UA server on port 1000 as HTTPS using the cert.pfx certificate. The password can be passed as an environment variable rather than on the command line. 

### Example 3
```powershell
PS C:\> Start-UAServer -Port 1000 -InProcess
```

Starts the UA server on port 1000 in the same process as the command is executing. If -InProcess is not included, a new process will be started to run the UA agent. 

### Example 3
```powershell
PS C:\> Start-UAServer -Port 1000 -ConnectionString C:\database.db
```

Starts the UA server on port 1000 with the connection string for the LiteDB database set to C:\database.db.

## PARAMETERS

### -CertificateFile
The certificate file to use. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
The certificate password to use. 

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
The path to the LiteDB database file. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GitRemote
The URL of the git remote to connect to. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GitRemoteCredential
Credentials for the Git remote. 

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InProcess
Runs the server in the current process. 

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

### -JwtAudience
The JWT audience used for generating JSON Web Tokens.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JwtIssuer
The JWT issuer used for generating JSON Web Tokens.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JwtSigningKey
The JWT signing used for generating JSON Web Tokens.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalComputerName
The name of the local computer. This defaults to localhost.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
The port to start to UA server on. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
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
