---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: 277790badbaeef02139034ffd32f639f90929133
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802085"
---
# <span data-ttu-id="3e1b4-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3e1b4-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="3e1b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1b4-103">新增主廚延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e1b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e1b4-104">SYNTAX</span></span>

### <span data-ttu-id="3e1b4-105">Linux</span><span class="sxs-lookup"><span data-stu-id="3e1b4-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1b4-106">時間</span><span class="sxs-lookup"><span data-stu-id="3e1b4-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="3e1b4-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1b4-108">**AzureVMChefExtension** Cmdlet 會將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="3e1b4-109">示例</span><span class="sxs-lookup"><span data-stu-id="3e1b4-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1b4-110">範例1：新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3e1b4-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="3e1b4-111">這個命令會將主廚延伸新增到名為 WindowsVM001 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="3e1b4-112">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="3e1b4-113">範例2：新增主廚延伸至 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3e1b4-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="3e1b4-114">這個命令會將主廚延伸新增到名為 LinuxVM001 的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="3e1b4-115">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="3e1b4-116">範例3：使用 [引導選項] 新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3e1b4-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="3e1b4-117">這個命令會將主廚延伸新增到名為 WindowsVM002 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="3e1b4-118">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="3e1b4-119">在引導之後，虛擬機器會參照 JSON 格式所指定的 BootstrapOptions。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="3e1b4-120">參數</span><span class="sxs-lookup"><span data-stu-id="3e1b4-120">PARAMETERS</span></span>

### <span data-ttu-id="3e1b4-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b4-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="3e1b4-122">-BootstrapOptions</span></span>
<span data-ttu-id="3e1b4-123">指定 [client_rb] 選項中的 [設定]。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b4-124">-BootstrapVersion</span></span>
<span data-ttu-id="3e1b4-125">指定啟動配置的版本。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="3e1b4-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="3e1b4-127">指定主廚服務執行的頻率 (（分鐘）) 。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="3e1b4-128">如果您不想要在 Azure VM 上安裝主廚服務，請將此欄位中的值設為0。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="3e1b4-129">-ChefServerUrl</span></span>
<span data-ttu-id="3e1b4-130">將主廚伺服器連結指定為 URL。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="3e1b4-131">-ClientRb</span></span>
<span data-ttu-id="3e1b4-132">指定主廚用戶端. rb 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-133">-守護程式</span><span class="sxs-lookup"><span data-stu-id="3e1b4-133">-Daemon</span></span>
<span data-ttu-id="3e1b4-134">為無人參與的執行設定主廚用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="3e1b4-135">節點平臺應該是 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-135">The node platform should be Windows.</span></span>
<span data-ttu-id="3e1b4-136">允許的選項： "none"、"service" 和 "task"。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="3e1b4-137">none-目前禁止主廚-用戶端服務被設定為服務。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="3e1b4-138">服務-將主廚用戶端設定為在背景中自動執行，成為服務。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="3e1b4-139">任務-將主廚-用戶端自動在背景中做為 secheduled 任務自動執行。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1b4-140">-DefaultProfile</span></span>
<span data-ttu-id="3e1b4-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e1b4-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="3e1b4-142">-JsonAttribute</span></span>
<span data-ttu-id="3e1b4-143">要新增至第一次執行主廚-用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="3e1b4-144">例如，-JsonAttribute "{" foo "：" bar "}"</span><span class="sxs-lookup"><span data-stu-id="3e1b4-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="3e1b4-145">-Linux</span></span>
<span data-ttu-id="3e1b4-146">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-147">-位置</span><span class="sxs-lookup"><span data-stu-id="3e1b4-147">-Location</span></span>
<span data-ttu-id="3e1b4-148">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e1b4-149">-Name</span></span>
<span data-ttu-id="3e1b4-150">指定主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="3e1b4-151">-OrganizationName</span></span>
<span data-ttu-id="3e1b4-152">指定主廚延伸的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-152">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1b4-153">-ResourceGroupName</span></span>
<span data-ttu-id="3e1b4-154">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="3e1b4-155">-RunList</span></span>
<span data-ttu-id="3e1b4-156">指定 [主廚] 節點的 [執行] 清單。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-156">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-157">密碼</span><span class="sxs-lookup"><span data-stu-id="3e1b4-157">-Secret</span></span>
<span data-ttu-id="3e1b4-158">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="3e1b4-159">-SecretFile</span></span>
<span data-ttu-id="3e1b4-160">檔案的路徑，該檔案包含用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b4-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="3e1b4-162">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="3e1b4-163">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="3e1b4-164">-ValidationPem</span></span>
<span data-ttu-id="3e1b4-165">指定主廚驗證程式. pem 檔路徑</span><span class="sxs-lookup"><span data-stu-id="3e1b4-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="3e1b4-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e1b4-166">-VMName</span></span>
<span data-ttu-id="3e1b4-167">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3e1b4-168">這個 Cmdlet 會為此參數指定的虛擬機器新增主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="3e1b4-169">-Windows</span></span>
<span data-ttu-id="3e1b4-170">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b4-171">-確認</span><span class="sxs-lookup"><span data-stu-id="3e1b4-171">-Confirm</span></span>
<span data-ttu-id="3e1b4-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1b4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1b4-173">-WhatIf</span></span>
<span data-ttu-id="3e1b4-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3e1b4-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1b4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1b4-176">CommonParameters</span></span>
<span data-ttu-id="3e1b4-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1b4-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1b4-179">輸入</span><span class="sxs-lookup"><span data-stu-id="3e1b4-179">INPUTS</span></span>

### <span data-ttu-id="3e1b4-180">所有</span><span class="sxs-lookup"><span data-stu-id="3e1b4-180">None</span></span>
<span data-ttu-id="3e1b4-181">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3e1b4-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e1b4-182">輸出</span><span class="sxs-lookup"><span data-stu-id="3e1b4-182">OUTPUTS</span></span>

### <span data-ttu-id="3e1b4-183">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3e1b4-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e1b4-184">筆記</span><span class="sxs-lookup"><span data-stu-id="3e1b4-184">NOTES</span></span>

## <span data-ttu-id="3e1b4-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e1b4-185">RELATED LINKS</span></span>

[<span data-ttu-id="3e1b4-186">AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3e1b4-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="3e1b4-187">移除-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3e1b4-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)