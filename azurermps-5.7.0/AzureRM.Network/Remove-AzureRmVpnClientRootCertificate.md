---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b86637618b0ef6a2ed337a48d5bdebf8888fad2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457436"
---
# <span data-ttu-id="f6c69-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c69-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="f6c69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6c69-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c69-103">移除現有的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="f6c69-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6c69-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6c69-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c69-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6c69-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c69-106">**AzureRmVpnClientRootCertificate** Cmdlet 會將指定的根憑證從虛擬網路閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="f6c69-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="f6c69-107">根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f6c69-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="f6c69-108">如果您移除使用憑證進行驗證的根憑證電腦，將無法再連線至閘道。</span><span class="sxs-lookup"><span data-stu-id="f6c69-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="f6c69-109">當您使用 **AzureRmVpnClientRootCertificate** 時，您必須同時提供憑證名稱和憑證資料的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="f6c69-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="f6c69-110">如需有關憑證之文字標記法的詳細資訊，請參閱 *PublicCertData* 參數說明。</span><span class="sxs-lookup"><span data-stu-id="f6c69-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="f6c69-111">示例</span><span class="sxs-lookup"><span data-stu-id="f6c69-111">EXAMPLES</span></span>

### <span data-ttu-id="f6c69-112">範例1：從虛擬網路閘道移除用戶端根憑證</span><span class="sxs-lookup"><span data-stu-id="f6c69-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="f6c69-113">這個範例會從虛擬網路閘道 ContosoVirtualGateway 中移除名為 ContosoRootCertificate 的用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="f6c69-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="f6c69-114">第一個命令使用 **取得內容** Cmdlet 來取得前一次匯出的憑證文字標記法;此文字標記法儲存在名為 $Text 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f6c69-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="f6c69-115">然後，第二個命令會使用 for 迴圈來提取 $Text 中除第一行和最後一行以外的所有文字。</span><span class="sxs-lookup"><span data-stu-id="f6c69-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="f6c69-116">這個提取的文字會儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f6c69-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="f6c69-117">第三個命令會使用儲存在 $CertificateText 變數中的資訊，以及 **AzureRmVpnClientRootCertificate** Cmdlet 來移除閘道的憑證。</span><span class="sxs-lookup"><span data-stu-id="f6c69-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="f6c69-118">參數</span><span class="sxs-lookup"><span data-stu-id="f6c69-118">PARAMETERS</span></span>

### <span data-ttu-id="f6c69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c69-119">-DefaultProfile</span></span>
<span data-ttu-id="f6c69-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6c69-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6c69-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="f6c69-121">-PublicCertData</span></span>
<span data-ttu-id="f6c69-122">指定要移除之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="f6c69-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="f6c69-123">若要取得文字標記法，請 (使用 Base64) 編碼將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="f6c69-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="f6c69-124">您應該會看到類似下列 (的輸出，請注意，實際的輸出會比以下) 所示的縮寫範例包含多行文字：</span><span class="sxs-lookup"><span data-stu-id="f6c69-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="f6c69-125">-----開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----[結束憑證]-----</span><span class="sxs-lookup"><span data-stu-id="f6c69-125">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="f6c69-126">PublicCertData 是由第一行之間的所有行所 (-----[開始憑證-----) ，而最後一行 (-----在檔案中-----[最終憑證 ) 。</span><span class="sxs-lookup"><span data-stu-id="f6c69-126">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="f6c69-127">您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData：</span><span class="sxs-lookup"><span data-stu-id="f6c69-127">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="f6c69-128">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="f6c69-128">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="f6c69-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c69-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6c69-130">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6c69-130">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="f6c69-131">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="f6c69-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f6c69-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f6c69-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f6c69-133">指定從中移除憑證的虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6c69-133">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="f6c69-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="f6c69-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="f6c69-135">指定此 Cmdlet 移除之用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6c69-135">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c69-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c69-136">CommonParameters</span></span>
<span data-ttu-id="f6c69-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6c69-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c69-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6c69-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c69-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f6c69-139">INPUTS</span></span>

### <span data-ttu-id="f6c69-140">所有</span><span class="sxs-lookup"><span data-stu-id="f6c69-140">None</span></span>
<span data-ttu-id="f6c69-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f6c69-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6c69-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f6c69-142">OUTPUTS</span></span>

## <span data-ttu-id="f6c69-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f6c69-143">NOTES</span></span>

## <span data-ttu-id="f6c69-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6c69-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6c69-145">附加 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c69-145">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="f6c69-146">AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c69-146">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="f6c69-147">新-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c69-147">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

