---
external help file: Az.Marketplace-help.xml
Module Name: Az.Marketplace
online version: https://learn.microsoft.com/powershell/module/az.marketplace/new-azmarketplaceprivatestorecollectionoffermulticontext
schema: 2.0.0
---

# New-AzMarketplacePrivateStoreCollectionOfferMultiContext

## SYNOPSIS
Upsert an offer with multiple context details.

## SYNTAX

### OfferExpanded (Default)
```
New-AzMarketplacePrivateStoreCollectionOfferMultiContext -OfferId <String> -CollectionId <String>
 -PrivateStoreId <String> [-ETag <String>] [-PlansContext <IContextAndPlansDetails[]>]
 [-PropertiesOfferId <String>] [-DefaultProfile <PSObject>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### OfferViaIdentityPrivateStoreExpanded
```
New-AzMarketplacePrivateStoreCollectionOfferMultiContext -OfferId <String> -CollectionId <String>
 -PrivateStoreInputObject <IMarketplaceIdentity> [-ETag <String>] [-PlansContext <IContextAndPlansDetails[]>]
 [-PropertiesOfferId <String>] [-DefaultProfile <PSObject>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### OfferViaIdentityCollectionExpanded
```
New-AzMarketplacePrivateStoreCollectionOfferMultiContext -OfferId <String>
 -CollectionInputObject <IMarketplaceIdentity> [-ETag <String>] [-PlansContext <IContextAndPlansDetails[]>]
 [-PropertiesOfferId <String>] [-DefaultProfile <PSObject>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### OfferViaIdentityExpanded
```
New-AzMarketplacePrivateStoreCollectionOfferMultiContext -OfferId <String> -InputObject <IMarketplaceIdentity>
 [-ETag <String>] [-PlansContext <IContextAndPlansDetails[]>] [-DefaultProfile <PSObject>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Upsert an offer with multiple context details.

## EXAMPLES

### EXAMPLE 1
```
$plan1 = @{
    context = "1f58b5dd-313c-42ed-84fc-f1e351bba7fb"
    planId = "plan1"
}
```

$plan2 = @{
    context = "ab3de7bc-7a6e-4e9f-a34a-f6922df453e4"
    planId = "plan2"
}

$plans = @($plan1,$plan2)

New-AzMarketplacePrivateStoreCollectionOfferMultiContext -CollectionId fdb889a1-cf3e-49f0-95b8-2bb012fa01f1 -PrivateStoreId a260d38c-96cf-492d-a340-404d0c4b3ad6  -OfferId test_pmc2pc1.vm_4plans -PlansContext $plans

## PARAMETERS

### -CollectionId
The collection ID

```yaml
Type: String
Parameter Sets: OfferExpanded, OfferViaIdentityPrivateStoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionInputObject
Identity Parameter
To construct, see NOTES section for COLLECTIONINPUTOBJECT properties and create a hash table.

```yaml
Type: IMarketplaceIdentity
Parameter Sets: OfferViaIdentityCollectionExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
The DefaultProfile parameter is not functional.
Use the SubscriptionId parameter when available if executing the cmdlet against a different subscription.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ETag
The offer's eTag.

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

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: IMarketplaceIdentity
Parameter Sets: OfferViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OfferId
The offer ID to update or delete

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

### -PlansContext
.
To construct, see NOTES section for PLANSCONTEXT properties and create a hash table.

```yaml
Type: IContextAndPlansDetails[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateStoreId
The store ID - must use the tenant ID

```yaml
Type: String
Parameter Sets: OfferExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateStoreInputObject
Identity Parameter
To construct, see NOTES section for PRIVATESTOREINPUTOBJECT properties and create a hash table.

```yaml
Type: IMarketplaceIdentity
Parameter Sets: OfferViaIdentityPrivateStoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PropertiesOfferId
The offer ID which contains the plans.

```yaml
Type: String
Parameter Sets: OfferExpanded, OfferViaIdentityPrivateStoreExpanded, OfferViaIdentityCollectionExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Marketplace.Models.IMarketplaceIdentity
## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Marketplace.Models.IOffer
## NOTES
COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties.
For information on hash tables, run Get-Help about_Hash_Tables.

COLLECTIONINPUTOBJECT \<IMarketplaceIdentity\>: Identity Parameter
  \[AdminRequestApprovalId \<String\>\]: The admin request approval ID to get create or update
  \[CollectionId \<String\>\]: The collection ID
  \[Id \<String\>\]: Resource identity path
  \[OfferId \<String\>\]: The offer ID to update or delete
  \[PrivateStoreId \<String\>\]: The store ID - must use the tenant ID
  \[RequestApprovalId \<String\>\]: The request approval ID to get create or update

INPUTOBJECT \<IMarketplaceIdentity\>: Identity Parameter
  \[AdminRequestApprovalId \<String\>\]: The admin request approval ID to get create or update
  \[CollectionId \<String\>\]: The collection ID
  \[Id \<String\>\]: Resource identity path
  \[OfferId \<String\>\]: The offer ID to update or delete
  \[PrivateStoreId \<String\>\]: The store ID - must use the tenant ID
  \[RequestApprovalId \<String\>\]: The request approval ID to get create or update

PLANSCONTEXT \<IContextAndPlansDetails\[\]\>: .
  \[Context \<String\>\]: Plan's context, e.g.
subscription ID, tenant ID.
  \[PlanId \<List\<String\>\>\]: List of plan IDs.

PRIVATESTOREINPUTOBJECT \<IMarketplaceIdentity\>: Identity Parameter
  \[AdminRequestApprovalId \<String\>\]: The admin request approval ID to get create or update
  \[CollectionId \<String\>\]: The collection ID
  \[Id \<String\>\]: Resource identity path
  \[OfferId \<String\>\]: The offer ID to update or delete
  \[PrivateStoreId \<String\>\]: The store ID - must use the tenant ID
  \[RequestApprovalId \<String\>\]: The request approval ID to get create or update

## RELATED LINKS

[https://learn.microsoft.com/powershell/module/az.marketplace/new-azmarketplaceprivatestorecollectionoffermulticontext](https://learn.microsoft.com/powershell/module/az.marketplace/new-azmarketplaceprivatestorecollectionoffermulticontext)

