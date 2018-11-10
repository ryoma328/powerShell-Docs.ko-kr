---
ms.date: 06/12/2017
contributor: JKeithB
keywords: gallery,powershell,cmdlet,psgallery
title: 호환되는 PowerShell 버전이 있는 패키지
ms.openlocfilehash: e16cfb0ee30e344c9399bec2985baafc5a252fd7
ms.sourcegitcommit: 98b7cfd8ad5718efa8e320526ca76c3cc4141d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50003784"
---
# <a name="packages-with-compatible-powershell-editions"></a><span data-ttu-id="727c6-103">호환되는 PowerShell 버전이 있는 패키지</span><span class="sxs-lookup"><span data-stu-id="727c6-103">Packages with compatible PowerShell Editions</span></span>

<span data-ttu-id="727c6-104">버전 5.1부터 PowerShell은 다양한 기능 집합 및 플랫폼 호환성을 나타내는 다양한 버전으로 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-104">Starting with version 5.1, PowerShell is available in different editions which denote varying feature sets and platform compatibility.</span></span>

- <span data-ttu-id="727c6-105">**Desktop Edition:** .NET Framework에서 구축되며 Server Core 및 Windows 데스크톱과 같은 전체 설치 공간 버전의 Windows에서 실행되는 PowerShell 버전을 대상으로 하는 스크립트 및 모듈과의 호환성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-105">**Desktop Edition:** Built on .NET Framework and provides compatibility with scripts and modules targeting versions of PowerShell running on full footprint editions of Windows such as Server Core and Windows Desktop.</span></span>
- <span data-ttu-id="727c6-106">**Core Edition:** .NET Core에서 구축되며 Nano Server 및 Windows IoT와 같은 축소된 설치 공간 버전의 Windows에서 실행되는 PowerShell 버전을 대상으로 하는 스크립트 및 모듈과의 호환성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-106">**Core Edition:** Built on .NET Core and provides compatibility with scripts and modules targeting versions of PowerShell running on reduced footprint editions of Windows such as Nano Server and Windows IoT.</span></span>

## <a name="powershell-gallery-extracts-supported-pseditions-metadata-and-allows-you-to-filters-the-packages-compatible-for-specific-powershell-editions"></a><span data-ttu-id="727c6-107">PowerShell 갤러리는 지원되는 PSEditions 메타데이터를 추출하며 특정 PowerShell 버전에 대해 호환되는 패키지를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-107">PowerShell Gallery extracts supported PSEditions metadata and allows you to filters the packages compatible for specific PowerShell Editions</span></span>

<span data-ttu-id="727c6-108">패키지에 호환되는 PSEditions가 지정된 경우 패키지 표시 페이지 및 패키지 결과에 'PowerShell 버전'의 일부로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-108">If a package has compatible PSEditions specified, they will be listed as part of 'PowerShell Editions' in the package display page and also in packages results.</span></span>

![PSEditions가 있는 항목 표시 페이지](../../Images/manual_package_download.png)

## <a name="search-for-packages-in-the-gallery-ui-which-works-on-powershellcore"></a><span data-ttu-id="727c6-110">갤러리 UI에서 PowerShellCore에 적용되는 패키지 검색</span><span class="sxs-lookup"><span data-stu-id="727c6-110">Search for packages in the gallery UI which works on PowerShellCore</span></span>

<span data-ttu-id="727c6-111">Tags:"PSEdition_Desktop" 및 Tags:"PSEdition_Core"를 사용하여 PowerShell 갤러리에 있는 패키지를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-111">Use Tags:"PSEdition_Desktop" and Tags:"PSEdition_Core" to filters the packages on PowerShell Gallery.</span></span>

### <a name="use-tagspseditioncore-to-search-items-compatible-with-powershell-core-edition"></a><span data-ttu-id="727c6-112">Tags:"PSEdition_Core"를 사용하여 PowerShell Core Edition과 호환되는 항목을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-112">Use Tags:"PSEdition_Core" to search items compatible with PowerShell Core Edition.</span></span>

![Core PSEdition과 호환되는 항목에 대한 검색 결과](../../Images/SearchResultsWithPSEditions.PNG)

### <a name="use-tagspseditiondesktop-to-search-items-compatible-with-powershell-desktop-edition"></a><span data-ttu-id="727c6-114">Tags:"PSEdition_Desktop"을 사용하여 PowerShell Desktop Edition과 호환되는 항목을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="727c6-114">Use Tags:"PSEdition_Desktop" to search items compatible with PowerShell Desktop Edition.</span></span>

![Desktop PSEdition과 호환되는 항목에 대한 검색 결과](../../Images/SearchResultsWithPSEdition-Desktop.PNG)

## <a name="more-details-on-authoring-and-finding-the-packages-with-compatible-powershell-editions"></a><span data-ttu-id="727c6-116">호환되는 PowerShell 버전이 있는 패키지를 작성 및 찾는 방법에 대한 자세한 내용</span><span class="sxs-lookup"><span data-stu-id="727c6-116">More details on authoring and finding the packages with compatible PowerShell Editions</span></span>

- [<span data-ttu-id="727c6-117">PSEditions가 있는 모듈</span><span class="sxs-lookup"><span data-stu-id="727c6-117">Modules with PSEditions</span></span>](../../concepts/module-psedition-support.md)
- [<span data-ttu-id="727c6-118">PSEditions가 있는 스크립트</span><span class="sxs-lookup"><span data-stu-id="727c6-118">Scripts with PSEditions</span></span>](../../concepts/script-psedition-support.md)
