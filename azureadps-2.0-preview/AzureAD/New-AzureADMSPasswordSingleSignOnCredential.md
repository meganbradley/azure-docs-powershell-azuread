---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSPasswordSingleSignOnCredential

## SYNOPSIS
Creates the password SSO credentials

## SYNTAX

```
New-AzureADMSPasswordSingleSignOnCredential -ObjectId <String> -PasswordSSOCredential <PasswordSSOCredentials>
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet enables users to create their Password Single-sign-on credentials for an application which they are part of.
Admin could create the group credentials as well.

## EXAMPLES

### New password single-sign-on credentials
```
PS C:\> $credentials = New-Object -TypeName Microsoft.Open.MSGraph.Model.PasswordSSOCredentials
PS C:\> $credentials.Id = "a4210a97-5e26-4cfe-88f1-118ed4886f27"
PS C:\> $creds1 = [Microsoft.Open.MSGraph.Model.PasswordSSOCredential]@{FieldId="param_1"; Value="foobar@ms.com"; Type="text"}
PS C:\> $creds2 = [Microsoft.Open.MSGraph.Model.PasswordSSOCredential]@{FieldId="param_2"; Value="my-secret"; Type="password"}
PS C:\> $credentials.Credentials = @($creds1, $creds2)

PS C:\> $new_creds_output = New-AzureADMSPasswordSingleSignOnCredential -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -PasswordSSOCredential $credentials
```

This command creates the password sso credentials for the given ObjectId and PasswordSSOObjectId.

## PARAMETERS

### -ObjectId
The unique identifier of the object specific Azure Active Directory object

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PasswordSSOCredential
User or group id

```yaml
Type: PasswordSSOCredentials
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.PasswordSSOCredentials
## NOTES
## RELATED LINKS
