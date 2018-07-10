---
ms.date: 06/12/2017
keywords: dsc,powershell,configuration,setup
title: MSFT_DSCLocalConfigurationManager 클래스의 ResourceGet 메서드
ms.openlocfilehash: 1b74adf2327af2e0f9416f1d00eac4e3b75e9013
ms.sourcegitcommit: 8b076ebde7ef971d7465bab834a3c2a32471ef6f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37893208"
---
# <a name="resourceget-method-of-the-msftdsclocalconfigurationmanager-class"></a><span data-ttu-id="73906-103">MSFT_DSCLocalConfigurationManager 클래스의 ResourceGet 메서드</span><span class="sxs-lookup"><span data-stu-id="73906-103">ResourceGet method of the MSFT_DSCLocalConfigurationManager class</span></span>

<span data-ttu-id="73906-104">DSC 리소스의 **Get** 메서드를 직접 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="73906-104">Directly calls the **Get** method of a DSC resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="73906-105">구문</span><span class="sxs-lookup"><span data-stu-id="73906-105">Syntax</span></span>

```mof
uint32 ResourceGet(
  [in]  string           ResourceType,
  [in]  string           ModuleName,
  [in]  uint8            resourceProperty[],
  [out] OMI_BaseResource configurations
);
```

## <a name="parameters"></a><span data-ttu-id="73906-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="73906-106">Parameters</span></span>

<span data-ttu-id="73906-107">*ResourceType* \[in\] 호출할 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73906-107">*ResourceType* \[in\] The name of the resource to call.</span></span>

<span data-ttu-id="73906-108">*ModuleName* \[in\] 호출할 리소스를 포함하는 모듈의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73906-108">*ModuleName* \[in\] The name of the module that contains the resource to call.</span></span>

<span data-ttu-id="73906-109">*resourceProperty* \[in\] 해시 테이블의 리소스 속성 이름과 해당 값을 각각 키와 값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73906-109">*resourceProperty* \[in\] Specifies the resource property name and its value in a hash table as key and value, respectively.</span></span> <span data-ttu-id="73906-110">[Get-DscResource](/powershell/module/PSDesiredStateConfiguration/Get-DscResource) cmdlet을 사용하여 리소스 속성 및 해당 종류를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="73906-110">Use the [Get-DscResource](/powershell/module/PSDesiredStateConfiguration/Get-DscResource) cmdlet to discover resource properties and their types.</span></span>

<span data-ttu-id="73906-111">*configurations* \[out\] 반환 시, 구성의 포함 인스턴스가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73906-111">*configurations* \[out\] On return, contains an embedded instance of the configurations.</span></span>

## <a name="return-value"></a><span data-ttu-id="73906-112">반환 값</span><span class="sxs-lookup"><span data-stu-id="73906-112">Return value</span></span>

<span data-ttu-id="73906-113">성공하면 0을 반환하고 그렇지 않으면 오류 코드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="73906-113">Returns zero on success; otherwise returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73906-114">설명</span><span class="sxs-lookup"><span data-stu-id="73906-114">Remarks</span></span>

<span data-ttu-id="73906-115">정적 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="73906-115">This is a static method.</span></span>

## <a name="requirements"></a><span data-ttu-id="73906-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="73906-116">Requirements</span></span>

<span data-ttu-id="73906-117">**MOF:** DscCore.mof</span><span class="sxs-lookup"><span data-stu-id="73906-117">**MOF:** DscCore.mof</span></span>

<span data-ttu-id="73906-118">**네임스페이스**: Root\Microsoft\Windows\DesiredStateConfiguration</span><span class="sxs-lookup"><span data-stu-id="73906-118">**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration</span></span>

## <a name="see-also"></a><span data-ttu-id="73906-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="73906-119">See also</span></span>

[<span data-ttu-id="73906-120">**MSFT_DSCLocalConfigurationManager**</span><span class="sxs-lookup"><span data-stu-id="73906-120">**MSFT_DSCLocalConfigurationManager**</span></span>](msft-dsclocalconfigurationmanager.md)