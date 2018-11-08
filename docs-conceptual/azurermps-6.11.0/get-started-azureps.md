---
title: 開始使用 Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 09/11/2018
ms.openlocfilehash: 5378cdb9d70aa0d2dc617d06d3c887ec20eb7767
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971783"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="2d0b1-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d0b1-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="2d0b1-103">Azure PowerShell 的設計是為了讓您從命令列管理 Azure 資源，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="2d0b1-104">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或者將它安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="2d0b1-105">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="2d0b1-106">安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d0b1-106">Install Azure PowerShell</span></span>

<span data-ttu-id="2d0b1-107">第一步是確定您已安裝最新版的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="2d0b1-108">如需最新版本的相關資訊，請參閱[版本資訊](./release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="2d0b1-109">[安裝 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="2d0b1-110">若要確認安裝是否成功，請從命令列執行 `Get-Module AzureRM -ListAvailable`。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-110">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="2d0b1-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="2d0b1-111">Azure Cloud Shell</span></span>

<span data-ttu-id="2d0b1-112">若要開始使用，最簡單的方式就是[啟動 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="2d0b1-113">從 Azure 入口網站的頂端導覽啟動 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 圖示](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="2d0b1-115">選擇您想使用的訂用帳戶，並建立儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![建立儲存體帳戶](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="2d0b1-117">一旦您建立儲存體之後，Cloud Shell 會在瀏覽器中開啟 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![適用於 PowerShell 的 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="2d0b1-119">您也可以安裝 Azure PowerShell，並在本機 PowerShell 工作階段中使用。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="2d0b1-120">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="2d0b1-120">Sign in to Azure</span></span>

<span data-ttu-id="2d0b1-121">以互動方式登入︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-121">Sign on interactively:</span></span>

1. <span data-ttu-id="2d0b1-122">輸入 `Connect-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="2d0b1-123">您會看到要求您提供 Azure 認證的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-123">You'll get a dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="2d0b1-124">選項 [-Environment] 可讓您驗證 Azure China 或 Azure Germany。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="2d0b1-125">例如 Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="2d0b1-125">for example, Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="2d0b1-126">輸入與您帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="2d0b1-127">Azure 會驗證並儲存認證資訊，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="2d0b1-128">在登入 Azure 帳戶後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="2d0b1-129">使用簡單的預設值建立 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2d0b1-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="2d0b1-130">`New-AzureRmVM` Cmdlet 提供簡化的語法，讓您能輕鬆地建立新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="2d0b1-131">您只需提供兩個參數值，分別是 VM 的名稱，以及一組 VM 上本機系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="2d0b1-132">首先，建立認證物件。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="2d0b1-133">接著，建立 VM。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="2d0b1-134">您可能會好奇是不是還建立了其他項目，以及 VM 是如何設定的。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-134">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="2d0b1-135">先來看看我們的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-135">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="2d0b1-136">您第一次使用 Cloud Shell 時會建立 **cloud-shell-storage-westus** 資源群組。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-136">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="2d0b1-137">**SampleVM** 資源群組是由 `New-AzureRmVM` Cmdlet 建立。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-137">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="2d0b1-138">現在，在這個新的資源群組中還建立了哪些其他的資源？</span><span class="sxs-lookup"><span data-stu-id="2d0b1-138">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="2d0b1-139">讓我們取得更多關於 VM 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-139">Let's get some more details about the VM.</span></span> <span data-ttu-id="2d0b1-140">此範例說明如何擷取用來建立 VM 的 OS 映像相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-140">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="2d0b1-141">建立設定完整的 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2d0b1-141">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="2d0b1-142">前面的範例使用簡化的語法和預設參數值來建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-142">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="2d0b1-143">在這個範例中，我們為虛擬機器提供所有選項的值。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-143">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="2d0b1-144">建立資源群組</span><span class="sxs-lookup"><span data-stu-id="2d0b1-144">Create a resource group</span></span>

<span data-ttu-id="2d0b1-145">在此範例中，我們要建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-145">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="2d0b1-146">對於您想要以邏輯方式群組在一起的多個資源，Azure 的資源群組可讓您有辦法管理這些資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-146">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="2d0b1-147">例如，您可以為應用程式或專案建立資源群組，並在該群組中新增虛擬機器、資料庫和 CDN 服務。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-147">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="2d0b1-148">讓我們建立一個名為「MyResourceGroup」的資源群組，位置則定在 Azure 的 westeurope 區域。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-148">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="2d0b1-149">若要這麼做，請輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="2d0b1-149">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="2d0b1-150">這個新的資源群組將會納入建立新 VM 所需的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-150">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="2d0b1-151">若要建立新的 Linux VM，我們必須先建立其他必要資源，並將它們指派至某組態。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-151">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="2d0b1-152">然後，我們可以使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-152">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="2d0b1-153">此外，您在使用者設定檔的 .ssh 目錄中需要有一個名為 `id_rsa.pub` 的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-153">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="2d0b1-154">建立必要的網路資源</span><span class="sxs-lookup"><span data-stu-id="2d0b1-154">Create the required network resources</span></span>

<span data-ttu-id="2d0b1-155">首先，我們需要建立一個子網路組態，以用於虛擬網路的建立程序。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-155">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="2d0b1-156">我們也會建立公用 IP 位址，以便可以連線到此 VM。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-156">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="2d0b1-157">我們會建立網路安全性群組，來保護對於公用位址的存取。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-157">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="2d0b1-158">最後，我們會使用前面的所有資源來建立虛擬 NIC。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-158">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="2d0b1-159">建立 VM 組態</span><span class="sxs-lookup"><span data-stu-id="2d0b1-159">Create the VM configuration</span></span>

<span data-ttu-id="2d0b1-160">我們已擁有所需的資源，可以建立 VM 組態物件了。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-160">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="2d0b1-161">建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2d0b1-161">Create the virtual machine</span></span>

<span data-ttu-id="2d0b1-162">現在，我們可以使用 VM 組態物件來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-162">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="2d0b1-163">VM 已建立完成，現在您可以搭配使用 SSH 與您所建立之 VM 的公用 IP 位址，來登入新的 Linux VM︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-163">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="2d0b1-164">在 Azure 中建立其他資源</span><span class="sxs-lookup"><span data-stu-id="2d0b1-164">Creating other resources in Azure</span></span>

<span data-ttu-id="2d0b1-165">我們已逐步瀏覽過如何建立資源群組、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-165">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="2d0b1-166">您也可以建立其他許多類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-166">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="2d0b1-167">例如，若要建立 Azure 網路負載平衡器，然後與我們新建立的 VM 相關聯，我們可以使用下列建立命令︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-167">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="2d0b1-168">我們也可以使用下列命令，為我們的基礎結構建立新的私人虛擬網路 (此網路在 Azure 中通常稱為「VNet」)︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-168">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="2d0b1-169">Azure 和 Azure PowerShell 的功能之所以強大，是因為它們不只能用來獲得雲端架構的基礎結構，還能用來建立受控平台服務。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-169">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="2d0b1-170">受控平台服務也可以結合基礎結構來建置更強大的解決方案。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-170">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="2d0b1-171">例如，您可以使用 Azure PowerShell 來建立 Azure AppService。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-171">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="2d0b1-172">Azure AppService 是一種受控平台服務，它可讓您裝載 Web 應用程式，而不必擔心基礎結構的問題。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-172">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="2d0b1-173">在建立 Azure AppService 之後，您可以使用下列命令在 AppService 內建立兩個新的 Azure Web Apps︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-173">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="2d0b1-174">列出已部署的資源</span><span class="sxs-lookup"><span data-stu-id="2d0b1-174">Listing deployed resources</span></span>

<span data-ttu-id="2d0b1-175">您可以使用 `Get-AzureRmResource` Cmdlet 來列出 Azure 內所執行的資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-175">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="2d0b1-176">下列範例顯示我們在新的資源群組中建立的資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-176">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="2d0b1-177">刪除資源</span><span class="sxs-lookup"><span data-stu-id="2d0b1-177">Deleting resources</span></span>

<span data-ttu-id="2d0b1-178">為了清除 Azure 帳戶，您想要移除我們已在此範例中建立的資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-178">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="2d0b1-179">您可以使用 `Remove-AzureRm*` Cmdlet 來刪除您不再需要的資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-179">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="2d0b1-180">若要移除我們已建立的 Windows VM，請使用下列命令︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-180">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="2d0b1-181">系統會提示您確認您想要移除資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-181">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2d0b1-182">您也可以一次刪除許多資源。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-182">You can also delete many resources at once.</span></span> <span data-ttu-id="2d0b1-183">例如，下列命令會刪除我們在目前為止的所有範例中使用的資源群組 "MyResourceGroup"。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-183">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="2d0b1-184">該群組中的所有資源也會一併刪除。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-184">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2d0b1-185">此工作可能需要幾分鐘才能完成，視資源的數量和類型而定。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-185">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="2d0b1-186">取得範例</span><span class="sxs-lookup"><span data-stu-id="2d0b1-186">Get samples</span></span>

<span data-ttu-id="2d0b1-187">若要深入了解如何使用 Azure PowerShell，請參閱我們針對 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 和 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 所提供的最常見指令碼。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-187">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2d0b1-188">後續步驟</span><span class="sxs-lookup"><span data-stu-id="2d0b1-188">Next steps</span></span>

* [<span data-ttu-id="2d0b1-189">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="2d0b1-189">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="2d0b1-190">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="2d0b1-190">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="2d0b1-191">使用 Azure PowerShell 在 Azure 中建立服務主體</span><span class="sxs-lookup"><span data-stu-id="2d0b1-191">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="2d0b1-192">參閱從較舊版本進行移轉的相關版本資訊：[https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes)。</span><span class="sxs-lookup"><span data-stu-id="2d0b1-192">Read the release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="2d0b1-193">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="2d0b1-193">Get help from the community:</span></span>
  * [<span data-ttu-id="2d0b1-194">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="2d0b1-194">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="2d0b1-195">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="2d0b1-195">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)