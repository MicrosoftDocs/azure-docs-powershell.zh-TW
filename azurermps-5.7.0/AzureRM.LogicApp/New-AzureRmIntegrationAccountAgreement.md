---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 838191018c50856f92f82699f7ac54686f1b3d97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624494"
---
# <span data-ttu-id="2ca77-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2ca77-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="2ca77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ca77-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca77-103">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2ca77-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca77-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ca77-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca77-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ca77-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca77-106">**新的-AzureRmIntegrationAccountAgreement** Cmdlet 會建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2ca77-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="2ca77-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="2ca77-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="2ca77-108">指定整合帳戶名稱、資源組名稱、協定名稱、類型、合作夥伴名稱、合作夥伴限定詞及協定內容。</span><span class="sxs-lookup"><span data-stu-id="2ca77-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="2ca77-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="2ca77-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="2ca77-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="2ca77-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2ca77-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="2ca77-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2ca77-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="2ca77-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2ca77-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="2ca77-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2ca77-114">示例</span><span class="sxs-lookup"><span data-stu-id="2ca77-114">EXAMPLES</span></span>

### <span data-ttu-id="2ca77-115">範例1：建立整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="2ca77-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="2ca77-116">這個命令會在指定的 Azure 資源群組中建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2ca77-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="2ca77-117">參數</span><span class="sxs-lookup"><span data-stu-id="2ca77-117">PARAMETERS</span></span>

### <span data-ttu-id="2ca77-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="2ca77-118">-AgreementContent</span></span>
<span data-ttu-id="2ca77-119">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="2ca77-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="2ca77-120">請指定此參數或 *AgreementContentFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="2ca77-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="2ca77-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="2ca77-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="2ca77-122">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2ca77-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="2ca77-123">請指定此參數或 *AgreementContent* 參數。</span><span class="sxs-lookup"><span data-stu-id="2ca77-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="2ca77-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="2ca77-124">-AgreementName</span></span>
<span data-ttu-id="2ca77-125">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca77-125">Specifies a name for the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="2ca77-126">-AgreementType</span></span>
<span data-ttu-id="2ca77-127">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="2ca77-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="2ca77-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2ca77-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ca77-129">X12</span><span class="sxs-lookup"><span data-stu-id="2ca77-129">X12</span></span> 
- <span data-ttu-id="2ca77-130">AS2</span><span class="sxs-lookup"><span data-stu-id="2ca77-130">AS2</span></span>
- <span data-ttu-id="2ca77-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="2ca77-131">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca77-132">-DefaultProfile</span></span>
<span data-ttu-id="2ca77-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ca77-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="2ca77-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="2ca77-135">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="2ca77-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="2ca77-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="2ca77-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="2ca77-137">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="2ca77-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="2ca77-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="2ca77-138">-GuestPartner</span></span>
<span data-ttu-id="2ca77-139">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca77-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="2ca77-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="2ca77-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="2ca77-141">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="2ca77-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="2ca77-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="2ca77-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="2ca77-143">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="2ca77-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="2ca77-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="2ca77-144">-HostPartner</span></span>
<span data-ttu-id="2ca77-145">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca77-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="2ca77-146">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2ca77-146">-Metadata</span></span>
<span data-ttu-id="2ca77-147">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="2ca77-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ca77-148">-Name</span></span>
<span data-ttu-id="2ca77-149">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca77-149">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca77-150">-ResourceGroupName</span></span>
<span data-ttu-id="2ca77-151">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca77-151">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-152">-確認</span><span class="sxs-lookup"><span data-stu-id="2ca77-152">-Confirm</span></span>
<span data-ttu-id="2ca77-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ca77-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca77-154">-WhatIf</span></span>
<span data-ttu-id="2ca77-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ca77-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca77-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ca77-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca77-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca77-157">CommonParameters</span></span>
<span data-ttu-id="2ca77-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ca77-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca77-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ca77-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca77-160">輸入</span><span class="sxs-lookup"><span data-stu-id="2ca77-160">INPUTS</span></span>

### <span data-ttu-id="2ca77-161">所有</span><span class="sxs-lookup"><span data-stu-id="2ca77-161">None</span></span>
<span data-ttu-id="2ca77-162">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2ca77-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ca77-163">輸出</span><span class="sxs-lookup"><span data-stu-id="2ca77-163">OUTPUTS</span></span>

### <span data-ttu-id="2ca77-164">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="2ca77-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="2ca77-165">筆記</span><span class="sxs-lookup"><span data-stu-id="2ca77-165">NOTES</span></span>

## <span data-ttu-id="2ca77-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ca77-166">RELATED LINKS</span></span>

[<span data-ttu-id="2ca77-167">AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2ca77-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="2ca77-168">移除-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2ca77-168">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="2ca77-169">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2ca77-169">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)

