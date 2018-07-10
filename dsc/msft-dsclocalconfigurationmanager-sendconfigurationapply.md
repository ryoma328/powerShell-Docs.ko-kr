---
ms.date: 06/12/2017
keywords: dsc,powershell,configuration,setup
title: MSFT_DSCLocalConfigurationManager 클래스의 SendConfigurationApply 메서드
ms.openlocfilehash: da3a08307122ab38ee4a6fd5d4a9b97579a988f7
ms.sourcegitcommit: 8b076ebde7ef971d7465bab834a3c2a32471ef6f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37893174"
---
# <a name="sendconfigurationapply-method-of-the-msftdsclocalconfigurationmanager-class"></a><span data-ttu-id="365b5-103">MSFT_DSCLocalConfigurationManager 클래스의 SendConfigurationApply 메서드</span><span class="sxs-lookup"><span data-stu-id="365b5-103">SendConfigurationApply method of the MSFT_DSCLocalConfigurationManager class</span></span>

<span data-ttu-id="365b5-104">구성 문서를 관리 노드로 보내고, 구성 에이전트를 사용해 구성을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="365b5-104">Sends the configuration document to the managed node and uses the Configuration Agent to apply the configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="365b5-105">구문</span><span class="sxs-lookup"><span data-stu-id="365b5-105">Syntax</span></span>

```mof
uint32 SendConfigurationApply(
  [in] uint8   ConfigurationData[],
  [in] boolean force
);
```

## <a name="parameters"></a><span data-ttu-id="365b5-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="365b5-106">Parameters</span></span>

<span data-ttu-id="365b5-107">*ConfigurationData* \[in\] 구성에 대한 환경 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="365b5-107">*ConfigurationData* \[in\] The environment data for the configuration.</span></span>

<span data-ttu-id="365b5-108">*force* \[in\] **true**이면 구성을 강제로 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="365b5-108">*force* \[in\] **true** to force the configuration to stop.</span></span>

## <a name="return-value"></a><span data-ttu-id="365b5-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="365b5-109">Return value</span></span>

<span data-ttu-id="365b5-110">성공하면 0을 반환하고 그렇지 않으면 오류 코드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="365b5-110">Returns zero on success; otherwise returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="365b5-111">설명</span><span class="sxs-lookup"><span data-stu-id="365b5-111">Remarks</span></span>

<span data-ttu-id="365b5-112">정적 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="365b5-112">This is a static method.</span></span>

## <a name="requirements"></a><span data-ttu-id="365b5-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="365b5-113">Requirements</span></span>

<span data-ttu-id="365b5-114">**MOF:** DscCore.mof</span><span class="sxs-lookup"><span data-stu-id="365b5-114">**MOF:** DscCore.mof</span></span>

<span data-ttu-id="365b5-115">**네임스페이스**: Root\Microsoft\Windows\DesiredStateConfiguration</span><span class="sxs-lookup"><span data-stu-id="365b5-115">**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration</span></span>

## <a name="see-also"></a><span data-ttu-id="365b5-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="365b5-116">See also</span></span>

[<span data-ttu-id="365b5-117">**MSFT_DSCLocalConfigurationManager**</span><span class="sxs-lookup"><span data-stu-id="365b5-117">**MSFT_DSCLocalConfigurationManager**</span></span>](msft-dsclocalconfigurationmanager.md)