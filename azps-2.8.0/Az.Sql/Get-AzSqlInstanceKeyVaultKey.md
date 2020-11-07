---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 8c17ca9f899adc731c549b45617c287010baaac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792771"
---
# <span data-ttu-id="e8c9b-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8c9b-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="e8c9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c9b-103">取得 SQL managed 實例的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="e8c9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8c9b-104">SYNTAX</span></span>

### <span data-ttu-id="e8c9b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8c9b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c9b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8c9b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c9b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8c9b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8c9b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8c9b-108">DESCRIPTION</span></span>
<span data-ttu-id="e8c9b-109">Get-AzSqlInstanceKeyVaultKey Cmdlet 會取得有關 SQL 管理實例上的主要保存庫金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="e8c9b-110">您可以透過提供 KeyId 來查看受管理實例上的所有金鑰，或查看特定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="e8c9b-111">示例</span><span class="sxs-lookup"><span data-stu-id="e8c9b-111">EXAMPLES</span></span>

### <span data-ttu-id="e8c9b-112">範例1：取得所有的主要保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="e8c9b-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e8c9b-113">這個命令會取得 SQL managed 實例上的所有主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="e8c9b-114">範例2：取得特定的金鑰保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="e8c9b-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e8c9b-115">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="e8c9b-116">範例3：使用實例物件</span><span class="sxs-lookup"><span data-stu-id="e8c9b-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e8c9b-117">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="e8c9b-118">範例4：使用實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8c9b-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e8c9b-119">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="e8c9b-120">範例5：使用管道</span><span class="sxs-lookup"><span data-stu-id="e8c9b-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e8c9b-121">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="e8c9b-122">參數</span><span class="sxs-lookup"><span data-stu-id="e8c9b-122">PARAMETERS</span></span>

### <span data-ttu-id="e8c9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c9b-123">-DefaultProfile</span></span>
<span data-ttu-id="e8c9b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-125">-實例</span><span class="sxs-lookup"><span data-stu-id="e8c9b-125">-Instance</span></span>
<span data-ttu-id="e8c9b-126">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="e8c9b-126">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e8c9b-127">-InstanceName</span></span>
<span data-ttu-id="e8c9b-128">實例名稱</span><span class="sxs-lookup"><span data-stu-id="e8c9b-128">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="e8c9b-129">-InstanceResourceId</span></span>
<span data-ttu-id="e8c9b-130">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8c9b-130">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e8c9b-131">-KeyId</span></span>
<span data-ttu-id="e8c9b-132">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="e8c9b-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c9b-133">-ResourceGroupName</span></span>
<span data-ttu-id="e8c9b-134">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e8c9b-134">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e8c9b-135">-Confirm</span></span>
<span data-ttu-id="e8c9b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c9b-137">-WhatIf</span></span>
<span data-ttu-id="e8c9b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c9b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c9b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c9b-140">CommonParameters</span></span>
<span data-ttu-id="e8c9b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c9b-142">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8c9b-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c9b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e8c9b-143">INPUTS</span></span>

### <span data-ttu-id="e8c9b-144">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="e8c9b-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="e8c9b-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e8c9b-145">System.String</span></span>

## <span data-ttu-id="e8c9b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e8c9b-146">OUTPUTS</span></span>

### <span data-ttu-id="e8c9b-147">AzureRmSqlManagedInstanceKeyVaultKeyModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="e8c9b-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="e8c9b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e8c9b-148">NOTES</span></span>

## <span data-ttu-id="e8c9b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8c9b-149">RELATED LINKS</span></span>