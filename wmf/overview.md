---
ms.date: 06/12/2018
keywords: wmf,powershell,setup
title: WMF(Windows Management Framework)
ms.openlocfilehash: 17011f88c364cb56a0c87f092873ccd99db450bc
ms.sourcegitcommit: 68093cc12a7a22c53d11ce7d33c18622921a0dd1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2018
ms.locfileid: "36943613"
---
# <a name="windows-management-framework"></a><span data-ttu-id="23ccc-103">Windows Management Framework</span><span class="sxs-lookup"><span data-stu-id="23ccc-103">Windows Management Framework</span></span>

<span data-ttu-id="23ccc-104">WMF(Windows Management Framework)는 Windows에 대한 일관적인 관리 인터페이스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="23ccc-104">Windows Management Framework (WMF) provides a consistent management interface for Windows.</span></span> <span data-ttu-id="23ccc-105">WMF는 다양한 버전의 Windows 클라이언트 및 Windows Server를 관리하는 원활한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="23ccc-105">WMF provides a seamless way to manage various versions of Windows client and Windows Server.</span></span> <span data-ttu-id="23ccc-106">WMF 설치 관리자 패키지는 관리 기능에 대한 업데이트를 포함하고 이전 버전의 Windows에 대해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="23ccc-106">WMF installer packages contain updates to management functionality and are available for older versions of Windows.</span></span>

<span data-ttu-id="23ccc-107">WMF 설치는 다음 기능을 추가 및/또는 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="23ccc-107">WMF installation adds and/or updates the following features:</span></span>

- <span data-ttu-id="23ccc-108">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="23ccc-108">Windows PowerShell</span></span>
- <span data-ttu-id="23ccc-109">Windows PowerShell DSC(원하는 상태 구성)</span><span class="sxs-lookup"><span data-stu-id="23ccc-109">Windows PowerShell Desired State Configuration (DSC)</span></span>
- <span data-ttu-id="23ccc-110">Windows PowerShell ISE(통합 스크립트 환경)</span><span class="sxs-lookup"><span data-stu-id="23ccc-110">Windows PowerShell Integrated Script Environment (ISE)</span></span>
- <span data-ttu-id="23ccc-111">WinRM(Windows Remote Management)</span><span class="sxs-lookup"><span data-stu-id="23ccc-111">Windows Remote Management (WinRM)</span></span>
- <span data-ttu-id="23ccc-112">WMI(Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="23ccc-112">Windows Management Instrumentation (WMI)</span></span>
- <span data-ttu-id="23ccc-113">Windows PowerShell 웹 서비스(관리 OData IIS 확장)</span><span class="sxs-lookup"><span data-stu-id="23ccc-113">Windows PowerShell Web Services (Management OData IIS Extension)</span></span>
- <span data-ttu-id="23ccc-114">소프트웨어 인벤토리 로깅(SIL)</span><span class="sxs-lookup"><span data-stu-id="23ccc-114">Software Inventory Logging (SIL)</span></span>
- <span data-ttu-id="23ccc-115">서버 관리자 CIM 공급자</span><span class="sxs-lookup"><span data-stu-id="23ccc-115">Server Manager CIM Provider</span></span>

## <a name="wmf-release-notes"></a><span data-ttu-id="23ccc-116">WMF 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="23ccc-116">WMF Release Notes</span></span>

<span data-ttu-id="23ccc-117">PowerShell 및 지정된 WMF의 다른 구성 요소에서 향상된 다양한 기능에 대해 알아보려면 아래 링크에서 릴리스 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="23ccc-117">To learn about various enhancements in PowerShell and other components of a given WMF, please refer to the links below to review the release notes:</span></span>

- [<span data-ttu-id="23ccc-118">WMF 5.1</span><span class="sxs-lookup"><span data-stu-id="23ccc-118">WMF 5.1</span></span>](5.1/release-notes.md)
- [<span data-ttu-id="23ccc-119">WMF 5.0</span><span class="sxs-lookup"><span data-stu-id="23ccc-119">WMF 5.0</span></span>](5.0/releasenotes.md)
- [<span data-ttu-id="23ccc-120">WMF 4.0</span><span class="sxs-lookup"><span data-stu-id="23ccc-120">WMF 4.0</span></span>](https://download.microsoft.com/download/3/D/6/3D61D262-8549-4769-A660-230B67E15B25/Windows%20Management%20Framework%204%200%20Release%20Notes.docx)
- [<span data-ttu-id="23ccc-121">WMF 3.0</span><span class="sxs-lookup"><span data-stu-id="23ccc-121">WMF 3.0</span></span>](https://download.microsoft.com/download/E/7/6/E76850B8-DA6E-4FF5-8CCE-A24FC513FD16/WMF%203%20Release%20Notes.docx)

## <a name="wmf-availability-across-windows-operating-systems"></a><span data-ttu-id="23ccc-122">Windows 운영 체제에서의 WMF 가용성</span><span class="sxs-lookup"><span data-stu-id="23ccc-122">WMF Availability Across Windows Operating Systems</span></span>

|<span data-ttu-id="23ccc-123">운영 체제 버전</span><span class="sxs-lookup"><span data-stu-id="23ccc-123">Operating System Version</span></span>  |<span data-ttu-id="23ccc-124">[WMF 5.1][]</span><span class="sxs-lookup"><span data-stu-id="23ccc-124">[WMF 5.1][]</span></span> |<span data-ttu-id="23ccc-125">[WMF 5.0][]</span><span class="sxs-lookup"><span data-stu-id="23ccc-125">[WMF 5.0][]</span></span> |<span data-ttu-id="23ccc-126">[WMF 4.0][]</span><span class="sxs-lookup"><span data-stu-id="23ccc-126">[WMF 4.0][]</span></span> |<span data-ttu-id="23ccc-127">[WMF 3.0][]</span><span class="sxs-lookup"><span data-stu-id="23ccc-127">[WMF 3.0][]</span></span>  |<span data-ttu-id="23ccc-128">[WMF 2.0][]</span><span class="sxs-lookup"><span data-stu-id="23ccc-128">[WMF 2.0][]</span></span> |
|--------------------------|------------|------------|------------|-------------|------------|
|<span data-ttu-id="23ccc-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="23ccc-129">Windows Server 2016</span></span>       |<span data-ttu-id="23ccc-130">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-130">Ships in-box</span></span>|            |            |             |            |
|<span data-ttu-id="23ccc-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="23ccc-131">Windows 10</span></span>                |<span data-ttu-id="23ccc-132">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-132">Ships in-box</span></span>|<span data-ttu-id="23ccc-133">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-133">Ships in-box</span></span>|            |             |            |
|<span data-ttu-id="23ccc-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="23ccc-134">Windows Server 2012 R2</span></span>    |<span data-ttu-id="23ccc-135">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-135">Yes</span></span>         |<span data-ttu-id="23ccc-136">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-136">Yes</span></span>         |<span data-ttu-id="23ccc-137">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-137">Ships in-box</span></span>|             |            |
|<span data-ttu-id="23ccc-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="23ccc-138">Windows 8.1</span></span>               |<span data-ttu-id="23ccc-139">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-139">Yes</span></span>         |<span data-ttu-id="23ccc-140">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-140">Yes</span></span>         |<span data-ttu-id="23ccc-141">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-141">Ships in-box</span></span>|             |            |
|<span data-ttu-id="23ccc-142">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23ccc-142">Windows Server 2012</span></span>       |<span data-ttu-id="23ccc-143">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-143">Yes</span></span>         |<span data-ttu-id="23ccc-144">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-144">Yes</span></span>         |<span data-ttu-id="23ccc-145">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-145">Yes</span></span>         |<span data-ttu-id="23ccc-146">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-146">Ships in-box</span></span> |            |
|<span data-ttu-id="23ccc-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="23ccc-147">Windows 8</span></span>                 |            |            |            |<span data-ttu-id="23ccc-148">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-148">Ships in-box</span></span> |            |
|<span data-ttu-id="23ccc-149">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="23ccc-149">Windows Server 2008 R2 SP1</span></span>|<span data-ttu-id="23ccc-150">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-150">Yes</span></span>         |<span data-ttu-id="23ccc-151">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-151">Yes</span></span>         |<span data-ttu-id="23ccc-152">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-152">Yes</span></span>         |<span data-ttu-id="23ccc-153">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-153">Yes</span></span>          |<span data-ttu-id="23ccc-154">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-154">Ships in-box</span></span>|
|<span data-ttu-id="23ccc-155">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="23ccc-155">Windows 7 SP1</span></span>             |<span data-ttu-id="23ccc-156">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-156">Yes</span></span>         |<span data-ttu-id="23ccc-157">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-157">Yes</span></span>         |<span data-ttu-id="23ccc-158">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-158">Yes</span></span>         |<span data-ttu-id="23ccc-159">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-159">Yes</span></span>          |<span data-ttu-id="23ccc-160">함께 제공</span><span class="sxs-lookup"><span data-stu-id="23ccc-160">Ships in-box</span></span>|
|<span data-ttu-id="23ccc-161">Windows Server 2008 SP2</span><span class="sxs-lookup"><span data-stu-id="23ccc-161">Windows Server 2008 SP2</span></span>   |            |            |            |<span data-ttu-id="23ccc-162">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-162">Yes</span></span>          |<span data-ttu-id="23ccc-163">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-163">Yes</span></span>         |
|<span data-ttu-id="23ccc-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23ccc-164">Windows Vista</span></span>             |            |            |            |             |<span data-ttu-id="23ccc-165">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-165">Yes</span></span>         |
|<span data-ttu-id="23ccc-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23ccc-166">Windows Server 2003</span></span>       |            |            |            |             |<span data-ttu-id="23ccc-167">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-167">Yes</span></span>         |
|<span data-ttu-id="23ccc-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="23ccc-168">Windows XP</span></span>                |            |            |            |<span data-ttu-id="23ccc-169">예</span><span class="sxs-lookup"><span data-stu-id="23ccc-169">Yes</span></span>          |            |

<span data-ttu-id="23ccc-170">**함께 제공**: 지정된 버전의 WMF 기능은 표시된 버전의 Windows 클라이언트 및 Windows Server에 제공되었습니다.</span><span class="sxs-lookup"><span data-stu-id="23ccc-170">**Ships in-box**: The features of the specified version of WMF were shipped in the indicated version of Windows client or Windows Server.</span></span>

[WMF 5.1]: https://aka.ms/wmf51download
[WMF 5.0]: https://aka.ms/wmf5download
[WMF 4.0]: https://aka.ms/wmf4download
[WMF 3.0]: https://aka.ms/wmf3download
[WMF 2.0]: https://aka.ms/wmf2download
