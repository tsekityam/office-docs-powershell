---
applicable: Exchange Server 2010
schema: 2.0.0
---

# Disable-OutlookAnywhere

## SYNOPSIS
This cmdlet is available only in Exchange Server 2010.

Use the Disable-OutlookAnywhere cmdlet to disable Outlook Anywhere on a computer running Exchange Server 2010 that has the Client Access server role installed.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

### Set1
```
Disable-OutlookAnywhere [-Identity] <VirtualDirectoryIdParameter> [-Confirm] [-DomainController <Fqdn>]
 [-WhatIf] [<CommonParameters>]
```

### Set2
```
Disable-OutlookAnywhere [-Confirm] [-DomainController <Fqdn>] [-Server <ServerIdParameter>] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The Disable-OutlookAnywhere cmdlet disables Outlook Anywhere on the Exchange 2010 Client Access server. This prevents the server from accepting requests from Microsoft Office Outlook 2007 and Outlook 2003 clients from the Internet by using Outlook Anywhere.

When you run this cmdlet, it can take as long as an hour for the settings to become effective, depending on how long it takes for Active Directory to replicate.

After the Client Access server is disabled for Outlook Anywhere, you may want to remove the RPC over HTTP proxy Windows networking component.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1
```
Disable-OutlookAnywhere -Server:CAS01
```

This example disables Outlook Anywhere on the Client Access server CAS01.

### Example 2
```
Disable-OutlookAnywhere -Identity: "exch01\rpc (Default Web Site)" -Confirm:$false
```

This example disables Outlook Anywhere on the Client Access server exch01 by specifying the Identity and Confirm parameters.

## PARAMETERS

### -Identity
The Identity parameter specifies the identity of the virtual directory that you want to disable.

```yaml
Type: VirtualDirectoryIdParameter
Parameter Sets: Set1
Aliases:
Applicable: Exchange Server 2010

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-* and Set-* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
The Server parameter specifies the name of the Client Access server to be disabled for Outlook Anywhere.

```yaml
Type: ServerIdParameter
Parameter Sets: Set2
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/6d345ef5-771e-43d5-8a15-28ac7c597d1f.aspx)

