---
ms.date: 06/12/2017
keywords: wmf,powershell,setup
ms.topic: conceptual
contributor: vaibch
title: 네트워크 스위치 관리자 cmdlet 오류
ms.openlocfilehash: a0f84c35974b6674faba4b0f19a28bd6e2490a96
ms.sourcegitcommit: 8b076ebde7ef971d7465bab834a3c2a32471ef6f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37893157"
---
# <a name="network-switch-manager-cmdlets-failure"></a><span data-ttu-id="e8462-103">네트워크 스위치 관리자 Cmdlet 오류</span><span class="sxs-lookup"><span data-stu-id="e8462-103">Network Switch Manager Cmdlets Failure</span></span>

<span data-ttu-id="e8462-104">네트워크 스위치 관리자 cmdlet을 사용하면 WSMAN을 통해 네트워크 스위치를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-104">The Network Switch Manager cmdlets can be used to manage network switches over WSMAN.</span></span>
<span data-ttu-id="e8462-105">이 모듈의 몇 가지 cmdlet에는 파이프라인을 통해 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-105">A few cmdlets of this module are capable of accepting values from pipelines.</span></span>
<span data-ttu-id="e8462-106">WMF 5.1 Preview에서는 파이프라인을 통해 값을 적용할 수 있는 cmdlet이 값이 파이프라인을 통해 전달되지 않는 경우 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-106">In WMF 5.1 Preview, the cmdlets that can accept value from pipeline fail to execute when the values are not passed through pipelines.</span></span>

<span data-ttu-id="e8462-107">"InputObject" 매개 변수를 사용하지 않는 경우 cmdlet이 오류 없이 계속 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-107">If "InputObject" parameter is not used, the cmdlet should continue to execute without failures.</span></span>

<span data-ttu-id="e8462-108">다음은 영향을 받는 cmdlet 목록입니다. 즉, 이러한 cmdlet은 파이프라인을 통해 "InputObject" 매개 변수의 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-108">Here is the list of affected cmdlets i.e. these cmdlets can accept value for "InputObject" parameter from pipeline.</span></span>
<span data-ttu-id="e8462-109">이 값이 파이프라인을 통해 전달되지 않는 경우 cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-109">If this value is not passed from pipeline the execution of cmdlet will fail.</span></span>

- <span data-ttu-id="e8462-110">Disable-NetworkSwitchEthernetPort</span><span class="sxs-lookup"><span data-stu-id="e8462-110">Disable-NetworkSwitchEthernetPort</span></span>
- <span data-ttu-id="e8462-111">Enable-NetworkSwitchEthernetPort</span><span class="sxs-lookup"><span data-stu-id="e8462-111">Enable-NetworkSwitchEthernetPort</span></span>
- <span data-ttu-id="e8462-112">Remove-NetworkSwitchEthernetPortIPAddress</span><span class="sxs-lookup"><span data-stu-id="e8462-112">Remove-NetworkSwitchEthernetPortIPAddress</span></span>
- <span data-ttu-id="e8462-113">Set-NetworkSwitchEthernetPortIPAddress</span><span class="sxs-lookup"><span data-stu-id="e8462-113">Set-NetworkSwitchEthernetPortIPAddress</span></span>
- <span data-ttu-id="e8462-114">Set-NetworkSwitchPortMode</span><span class="sxs-lookup"><span data-stu-id="e8462-114">Set-NetworkSwitchPortMode</span></span>
- <span data-ttu-id="e8462-115">Set-NetworkSwitchPortProperty</span><span class="sxs-lookup"><span data-stu-id="e8462-115">Set-NetworkSwitchPortProperty</span></span>
- <span data-ttu-id="e8462-116">Disable-NetworkSwitchFeature</span><span class="sxs-lookup"><span data-stu-id="e8462-116">Disable-NetworkSwitchFeature</span></span>
- <span data-ttu-id="e8462-117">Enable-NetworkSwitchFeature</span><span class="sxs-lookup"><span data-stu-id="e8462-117">Enable-NetworkSwitchFeature</span></span>
- <span data-ttu-id="e8462-118">Remove-NetworkSwitchVlan</span><span class="sxs-lookup"><span data-stu-id="e8462-118">Remove-NetworkSwitchVlan</span></span>
- <span data-ttu-id="e8462-119">Set-NetworkSwitchVlanProperty</span><span class="sxs-lookup"><span data-stu-id="e8462-119">Set-NetworkSwitchVlanProperty</span></span>

## <a name="resolution"></a><span data-ttu-id="e8462-120">해결 방법</span><span class="sxs-lookup"><span data-stu-id="e8462-120">Resolution</span></span>

<span data-ttu-id="e8462-121">InputObject 매개 변수 값을 파이프라인을 통해 전달하면 cmdlet이 올바로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-121">The cmdlets work fine when the value of InputObject parameter are passed into it through pipeline.</span></span> <span data-ttu-id="e8462-122">위의 cmdlet에 대해 작동하는 몇 가지 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8462-122">A few examples that work for the above cmdlets are:</span></span>

- `Disable-NetworkSwitchEthernetPort`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Disable-NetworkSwitchEthernetPort -CimSession $cimSession
  ```

- `Enable-NetworkSwitchEthernetPort`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Enable-NetworkSwitchEthernetPort -CimSession $cimSession
  ```

- `Remove-NetworkSwitchEthernetPortIPAddress`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Remove-NetworkSwitchEthernetPortIPAddress -CimSession $cimSession
  ```

- `Set-NetworkSwitchEthernetPortIPAddress`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $ipAddress = "192.168.10.1"
  $subnetAddress = "255.255.255.0"
  $port | Set-NetworkSwitchEthernetPortIPAddress -IpAddress $ipAddress -SubnetAddress $subnetAddress -CimSession $cimSession
  ```

- `Set-NetworkSwitchPortProperty`

  ```powershell
  $portProperties = @{Caption = "New Caption"}
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Set-NetworkSwitchPortProperty -Property $portProperties -CimSession $cimSession
  ```

- `Disable-NetworkSwitchFeature`

  ```powershell
  $feature = Get-CimInstance -Namespace root/interop -ClassName MSFT_Feature -CimSession $cimSession | Select-Object -First 1
  $feature | Disable-NetworkSwitchFeature -CimSession $cimSession
  ```

- `Enable-NetworkSwitchFeature`

  ```powershell
  $feature = Get-CimInstance -Namespace root/interop -ClassName MSFT_Feature -CimSession $cimSession | Select-Object -First 1
  $feature | Enable-NetworkSwitchFeature -CimSession $cimSession
  ```

- `Set-NetworkSwitchVlanProperty`

  ```powershell
  $properties = @{Caption = "New Caption"}
  $vlan = Get-CimInstance -ClassName CIM_NetworkVlan -Namespace root/interop -CimSession $cimSession | Select-Object -First 1
  $vlan | Set-NetworkSwitchVlanProperty -Property $properties -CimSession $cimSession
  ```