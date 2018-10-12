---
ms.date: 06/12/2017
contributor: JKeithB
keywords: gallery,powershell,cmdlet,psgallery
title: PowerShell 갤러리 시작
ms.openlocfilehash: 39998df1a2bf9363dd008dc96a802157c8d691d7
ms.sourcegitcommit: e46b868f56f359909ff7c8230b1d1770935cce0e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45523059"
---
# <a name="get-started-with-the-powershell-gallery"></a><span data-ttu-id="8f797-103">PowerShell 갤러리 시작</span><span class="sxs-lookup"><span data-stu-id="8f797-103">Get Started with the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-104">PowerShell 갤러리에서 항목을 설치하는 올바른 방법은 [PowerShellGet](/powershell/module/powershellget) 모듈에서 cmdlet을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-104">The proper way to install items from the PowerShell Gallery is to use the cmdlets in the [PowerShellGet](/powershell/module/powershellget) module.</span></span> <span data-ttu-id="8f797-105">PowerShell 갤러리에서 항목을 다운로드하기 위해 로그인할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-105">You do not need to sign in to download items from the PowerShell Gallery.</span></span>

> [!NOTE]
> <span data-ttu-id="8f797-106">패키지는 PowerShell 갤러리에서 직접 다운로드할 수 있지만 권장되는 방법이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-106">It is possible to download a package from the PowerShell Gallery directly, but this is not a recommended approach.</span></span> <span data-ttu-id="8f797-107">자세한 내용은 [수동 패키지 다운로드](https://msdn.microsoft.com/en-us/powershell/gallery/psgallery/how-to/working-with-items/manual-download.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8f797-107">For more details, see [Manual Package Download](https://msdn.microsoft.com/en-us/powershell/gallery/psgallery/how-to/working-with-items/manual-download.md).</span></span>  


## <a name="discovering-items-from-the-powershell-gallery"></a><span data-ttu-id="8f797-108">PowerShell 갤러리에서 항목 검색</span><span class="sxs-lookup"><span data-stu-id="8f797-108">Discovering items from the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-109">이 웹 사이트에서 **검색** 컨트롤을 사용하거나 모듈 및 스크립트 페이지를 검색하여 PowerShell 갤러리에서 항목을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-109">You can find items in the PowerShell Gallery by using the **Search** control on this website, or by browsing through the Modules and Scripts pages.</span></span> <span data-ttu-id="8f797-110">항목 유형에 따라 [Find-Module][] 및 [Find-Script][] cmdlet을 `-Repository PSGallery`와 함께 사용하여 PowerShell 갤러리에서 항목을 찾을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-110">You can also find items from the PowerShell Gallery by running the [Find-Module][] and [Find-Script][] cmdlets, depending on the item type, with `-Repository PSGallery`.</span></span>

<span data-ttu-id="8f797-111">다음 매개 변수를 사용하여 갤러리의 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-111">Filtering results from the Gallery can be done by using the following parameters:</span></span>

- <span data-ttu-id="8f797-112">Name</span><span class="sxs-lookup"><span data-stu-id="8f797-112">Name</span></span>
- <span data-ttu-id="8f797-113">AllVersions</span><span class="sxs-lookup"><span data-stu-id="8f797-113">AllVersions</span></span>
- <span data-ttu-id="8f797-114">MinimumVersion</span><span class="sxs-lookup"><span data-stu-id="8f797-114">MinimumVersion</span></span>
- <span data-ttu-id="8f797-115">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8f797-115">RequiredVersion</span></span>
- <span data-ttu-id="8f797-116">태그</span><span class="sxs-lookup"><span data-stu-id="8f797-116">Tag</span></span>
- <span data-ttu-id="8f797-117">Includes</span><span class="sxs-lookup"><span data-stu-id="8f797-117">Includes</span></span>
- <span data-ttu-id="8f797-118">DscResource</span><span class="sxs-lookup"><span data-stu-id="8f797-118">DscResource</span></span>
- <span data-ttu-id="8f797-119">RoleCapability</span><span class="sxs-lookup"><span data-stu-id="8f797-119">RoleCapability</span></span>
- <span data-ttu-id="8f797-120">명령</span><span class="sxs-lookup"><span data-stu-id="8f797-120">Command</span></span>
- <span data-ttu-id="8f797-121">필터</span><span class="sxs-lookup"><span data-stu-id="8f797-121">Filter</span></span>

<span data-ttu-id="8f797-122">갤러리에서 특정 DSC 리소스를 검색하는 데만 관심이 있는 경우 [Find-DscResource] cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-122">If you're only interested in discovering specific DSC resources in the Gallery, you can run the [Find-DscResource] cmdlet.</span></span> <span data-ttu-id="8f797-123">Find-DscResource는 갤러리에 포함된 DSC 리소스에 대한 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-123">Find-DscResource returns data on DSC resources contained in the Gallery.</span></span>
<span data-ttu-id="8f797-124">DSC 리소스는 항상 모듈의 일부로 제공되기 때문에 여전히 [Install-Module][]을 실행하여 이러한 DSC 리소스를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-124">Because DSC resources are always delivered as part of a module, you still need to run [Install-Module][] to install those DSC resources.</span></span>

## <a name="learning-about-items-in-the-powershell-gallery"></a><span data-ttu-id="8f797-125">PowerShell 갤러리에 있는 항목에 대해 알아보기</span><span class="sxs-lookup"><span data-stu-id="8f797-125">Learning about items in the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-126">관심 있는 항목을 식별했으면 자세히 알아보는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-126">Once you've identified an item you're interested in, you may want to learn more about it.</span></span> <span data-ttu-id="8f797-127">이렇게 하려면 갤러리에서 해당 항목의 특정 페이지를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-127">You can do this by examining that item's specific page on the Gallery.</span></span> <span data-ttu-id="8f797-128">이 페이지에서 항목과 함께 업로드된 메타데이터를 모두 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-128">On that page, you'll be able to see all of the metadata uploaded with the item.</span></span> <span data-ttu-id="8f797-129">항목에 대한 이 메타데이터는 항목의 작성자가 제공하며 Microsoft에서 확인하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-129">This metadata for an item is provided by the item's author, and is not verified by Microsoft.</span></span> <span data-ttu-id="8f797-130">항목의 소유자는 항목을 게시하는 데 사용되는 갤러리 계정에 강하게 연결되어 있으며 작성자 필드보다 더 신뢰할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-130">The Owner of the item is strongly tied to the Gallery account used to publish the item, and is more trustworthy than the Author field.</span></span>

<span data-ttu-id="8f797-131">좋은 의도에서 게시되지 않은 것 같은 항목을 발견할 경우 해당 항목의 페이지에서 **신고하기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-131">If you discover an item that you feel is not published in good faith, click **Report Abuse** on that item's page.</span></span>

<span data-ttu-id="8f797-132">[Find-Module][] 또는 [Find-Script][]를 실행하는 경우 반환된 PSGetModuleInfo 개체에서 이 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-132">If you're running [Find-Module][] or [Find-Script][], you can view this data in the returned PSGetModuleInfo object.</span></span> <span data-ttu-id="8f797-133">예를 들어 `Find-Module -Name PSReadLine -Repository PSGallery |Get-Member`를 실행하면</span><span class="sxs-lookup"><span data-stu-id="8f797-133">For example, running `Find-Module -Name PSReadLine -Repository PSGallery |Get-Member`</span></span>
<span data-ttu-id="8f797-134">갤러리에서 PSReadLine 모듈의 데이터가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-134">returns data on the PSReadLine module in the Gallery.</span></span>

## <a name="downloading-items-from-the-powershell-gallery"></a><span data-ttu-id="8f797-135">PowerShell 갤러리에서 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="8f797-135">Downloading items from the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-136">PowerShell 갤러리에서 항목을 다운로드하는 경우 다음 프로세스를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-136">We encourage the following process when downloading items from the PowerShell Gallery:</span></span>

### <a name="inspect"></a><span data-ttu-id="8f797-137">검사</span><span class="sxs-lookup"><span data-stu-id="8f797-137">Inspect</span></span>

<span data-ttu-id="8f797-138">검사를 위해 갤러리에서 항목을 다운로드하려면 항목 유형에 따라 [Save-Module][] 또는 [Save-Script][] cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-138">To download an item from the Gallery for inspection, run either the [Save-Module][] or [Save-Script][] cmdlet, depending on the item type.</span></span> <span data-ttu-id="8f797-139">이렇게 하면 설치하지 않고 로컬에 항목을 저장한 다음 항목 내용을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-139">This lets you save the item locally without installing it, and inspect the item contents.</span></span> <span data-ttu-id="8f797-140">저장된 항목을 수동으로 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-140">Remember to delete the saved item manually.</span></span>

<span data-ttu-id="8f797-141">이러한 항목 중 일부는 Microsoft에서 작성되었으며 다른 항목은 PowerShell 커뮤니티에서 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-141">Some of these items are authored by Microsoft, and others are authored by the PowerShell community.</span></span>
<span data-ttu-id="8f797-142">설치 전에 이 갤러리에 있는 항목의 내용과 코드를 검토하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-142">Microsoft recommends that you review the contents and code of items on this gallery prior to installation.</span></span>

<span data-ttu-id="8f797-143">좋은 의도에서 게시되지 않은 것 같은 항목을 발견할 경우 해당 항목의 페이지에서 **신고하기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-143">If you discover an item that you feel is not published in good faith, click **Report Abuse** on that item's page.</span></span>

### <a name="install"></a><span data-ttu-id="8f797-144">설치</span><span class="sxs-lookup"><span data-stu-id="8f797-144">Install</span></span>

<span data-ttu-id="8f797-145">사용을 위해 갤러리에서 항목을 설치하려면 항목 유형에 따라 [Install-Module][] 또는 [Install-Script][] cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-145">To install an item from the Gallery for use, run either the [Install-Module][] or [Install-Script][] cmdlet, depending on the item type.</span></span>

<span data-ttu-id="8f797-146">[Install-Module][]은 기본적으로 `$env:ProgramFiles\WindowsPowerShell\Modules`에 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-146">[Install-Module][] installs the module to `$env:ProgramFiles\WindowsPowerShell\Modules` by default.</span></span>
<span data-ttu-id="8f797-147">이 경우 관리자 계정이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-147">This requires an administrator account.</span></span> <span data-ttu-id="8f797-148">`-Scope CurrentUser` 매개 변수를 추가하는 경우 모듈은 `$env:USERPROFILE\Documents\WindowsPowerShell\Modules`에 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-148">If you add the `-Scope CurrentUser` parameter, the module is installed to `$env:USERPROFILE\Documents\WindowsPowerShell\Modules` .</span></span>

<span data-ttu-id="8f797-149">[Install-Script][]는 기본적으로 `$env:ProgramFiles\WindowsPowerShell\Scripts`에 스크립트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-149">[Install-Script][] installs the script to `$env:ProgramFiles\WindowsPowerShell\Scripts` by default.</span></span>
<span data-ttu-id="8f797-150">이 경우 관리자 계정이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-150">This requires an administrator account.</span></span> <span data-ttu-id="8f797-151">`-Scope CurrentUser` 매개 변수를 추가하는 경우 스크립트는 `$env:USERPROFILE\Documents\WindowsPowerShell\Scripts`에 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-151">If you add the `-Scope CurrentUser` parameter, the script is installed to `$env:USERPROFILE\Documents\WindowsPowerShell\Scripts` .</span></span>

<span data-ttu-id="8f797-152">기본적으로 [Install-Module][] 및 [Install-Script][]는 최신 버전의 항목을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-152">By default, [Install-Module][] and [Install-Script][] installs the most current version of an item.</span></span>
<span data-ttu-id="8f797-153">이전 버전의 항목을 설치하려면 `-RequiredVersion` 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-153">To install an older version of the item, add the `-RequiredVersion` parameter.</span></span>

### <a name="deploy"></a><span data-ttu-id="8f797-154">배포 게스트 클러스터에</span><span class="sxs-lookup"><span data-stu-id="8f797-154">Deploy</span></span>

<span data-ttu-id="8f797-155">PowerShell 갤러리의 항목을 Azure Automation에 배포하려면 항목 세부 정보 페이지에서 **Azure Automation에 배포**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-155">To deploy an item from the PowerShell Gallery to Azure Automation, click **Deploy to Azure Automation** on the item details page.</span></span> <span data-ttu-id="8f797-156">Azure 관리 포털로 리디렉션되며, 여기서 Azure 계정 자격 증명을 사용하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-156">You will be redirected to the Azure Management Portal, where you sign in by using your Azure account credentials.</span></span> <span data-ttu-id="8f797-157">종속성과 함께 항목을 배포하면 모든 종속성이 Azure Automation에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-157">Note that deploying items with dependencies will deploy all the dependencies to Azure Automation.</span></span> <span data-ttu-id="8f797-158">항목 메타데이터에 **AzureAutomationNotSupported** 태그를 추가하면 'Azure Automation에 배포' 단추를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-158">The 'Deploy to Azure Automation' button can be disabled by adding the **AzureAutomationNotSupported** tag to your item metadata.</span></span>

<span data-ttu-id="8f797-159">Azure Automation에 대한 자세한 내용은 [Azure Automation](/azure/automation) 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8f797-159">To learn more about Azure Automation, see the [Azure Automation](/azure/automation) documentation.</span></span>

## <a name="updating-items-from-the-powershell-gallery"></a><span data-ttu-id="8f797-160">PowerShell 갤러리에서 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="8f797-160">Updating items from the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-161">PowerShell 갤러리에서 설치된 항목을 업데이트하려면 [Update-Module][] 또는 [Update-Script][] cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-161">To update items installed from the PowerShell Gallery, run either the [Update-Module][] or [Update-Script][] cmdlet.</span></span> <span data-ttu-id="8f797-162">추가 매개 변수 없이 실행하면 [Update-Module][]이 [Install-Module][]을 실행하여 설치된 각 모듈을 업데이트하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-162">When run without any additional parameters, [Update-Module][] attempts to update each module installed by running [Install-Module][].</span></span> <span data-ttu-id="8f797-163">모듈을 선택적으로 업데이트하려면 `-Name` 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-163">To selectively update modules, add the `-Name` parameter.</span></span>

<span data-ttu-id="8f797-164">마찬가지로, 추가 매개 변수 없이 실행하면 [Update-Script][]는 [Install-Script][]를 실행하여 설치된 각 스크립트를 업데이트하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-164">Similarly, when run without any additional parameters, [Update-Script][] also attempts to update each script installed by running [Install-Script][].</span></span> <span data-ttu-id="8f797-165">스크립트를 선택적으로 업데이트하려면 `-Name` 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-165">To selectively update scripts, add the `-Name` parameter.</span></span>

## <a name="list-items-that-you-have-installed-from-the-powershell-gallery"></a><span data-ttu-id="8f797-166">PowerShell 갤러리에서 설치한 항목 나열</span><span class="sxs-lookup"><span data-stu-id="8f797-166">List items that you have installed from the PowerShell Gallery</span></span>

<span data-ttu-id="8f797-167">PowerShell 갤러리에서 설치한 모듈을 찾으려면 [Get-InstalledModule][] cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-167">To find out which modules you have installed from the PowerShell Gallery, run the [Get-InstalledModule][] cmdlet.</span></span> <span data-ttu-id="8f797-168">이 명령은 PowerShell 갤러리에서 직접 설치된 시스템의 모듈을 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-168">This command lists all of the modules you have on your system that were installed directly from the PowerShell Gallery.</span></span>

<span data-ttu-id="8f797-169">마찬가지로, PowerShell 갤러리에서 설치한 스크립트를 찾으려면 [Get-InstalledScript][] cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-169">Similarly, to find out which scripts you have installed from the PowerShell Gallery, run the [Get-InstalledScript][] cmdlet.</span></span> <span data-ttu-id="8f797-170">이 명령은 PowerShell 갤러리에서 직접 설치된 시스템의 스크립트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f797-170">This command lists all of the scripts you have on your system that were installed directly from the PowerShell Gallery.</span></span>

[Find-DscResource]: /powershell/module/powershellget/Find-DscResource
[Find-Module]: /powershell/module/powershellget/Find-Module
[Find-Script]: /powershell/module/powershellget/Find-Script
[Get-InstalledModule]: /powershell/module/powershellget/Get-InstalledModule
[Get-InstalledScript]: /powershell/module/powershellget/Get-InstalledScript
[Install-Module]: /powershell/module/powershellget/Install-Module
[Install-Script]: /powershell/module/powershellget/Install-Script
[Publish-Module]: /powershell/module/powershellget/Publish-Module
[Publish-Script]: /powershell/module/powershellget/Publish-Script
[Register-PSRepository]: /powershell/module/powershellget/Register-Repository
[Save-Module]: /powershell/module/powershellget/Save-Module
[Save-Script]: /powershell/module/powershellget/Save-Script