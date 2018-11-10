---
ms.date: 06/12/2017
contributor: JKeithB
keywords: gallery,powershell,cmdlet,psgallery
title: 갤러리 검색 구문
ms.openlocfilehash: 9aadb6771c85845cc3fa05cb56f0194b060d1c1b
ms.sourcegitcommit: 98b7cfd8ad5718efa8e320526ca76c3cc4141d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50003776"
---
# <a name="gallery-search-syntax"></a><span data-ttu-id="6997d-103">갤러리 검색 구문</span><span class="sxs-lookup"><span data-stu-id="6997d-103">Gallery Search Syntax</span></span>

<span data-ttu-id="6997d-104">PowerShell 갤러리는 단어, 구 및 키워드 식을 사용하여 검색 결과 범위를 좁힐 수 있는 텍스트 검색 상자를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-104">PowerShell Gallery offers a text searchbox where you can use words, phrases and keyword expressions to narrow down search results.</span></span>

## <a name="search-by-keywords"></a><span data-ttu-id="6997d-105">키워드로 검색</span><span class="sxs-lookup"><span data-stu-id="6997d-105">Search by Keywords</span></span>

    dsc azure sql

<span data-ttu-id="6997d-106">검색은 3가지 키워드를 모두 포함하는 관련 문서를 찾으려고 하며 일치하는 문서를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-106">Search will do its best effort to find relevant documents containing all 3 keywords, and return matching documents.</span></span>

## <a name="search-using-phrases-and-keywords"></a><span data-ttu-id="6997d-107">구문 및 키워드를 사용하여 검색</span><span class="sxs-lookup"><span data-stu-id="6997d-107">Search using Phrases and keywords</span></span>

    "azure sql" deployment

<span data-ttu-id="6997d-108">따옴표("") 사이에 구를 입력하면 별도 키워드가 아닌 특정 구를 찾도록 검색이 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-108">Entering a phrase between quotation marks ("") change the search to look for the particular phrase instead of separate keywords.</span></span>
<span data-ttu-id="6997d-109">일반적으로 일치하는 문서에는 대/소문자 변형(예: "Azure SQL")을 포함하여 "azure sql" 구가 정확하게 포함되어야 하며, 대체로 '배포'라는 단어도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-109">Matching documents should usually contain the exact phrase "azure sql", including variations on capitalization e.g. "Azure SQL", and also usually contain the word 'deployment'.</span></span>

## <a name="filtering-on-fields"></a><span data-ttu-id="6997d-110">필드 필터링</span><span class="sxs-lookup"><span data-stu-id="6997d-110">Filtering on fields</span></span>

<span data-ttu-id="6997d-111">특정 패키지 ID(또는 'Id' 또는 'id')를 검색하거나 검색어 앞에 필드 이름을 추가하여 다른 특정 필드를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-111">You can search for a specific package ID (or 'Id' or 'id'), or certain other fields by prefixing search terms with the field name.</span></span>

<span data-ttu-id="6997d-112">현재 검색 가능한 필드는 'Id', 'Version', 'Tags', 'Author', 'Owner', 'Functions', 'Cmdlets', 'DscResources' 및 'PowerShellVersion'입니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-112">Currently the searchable fields are 'Id', 'Version', 'Tags', 'Author', 'Owner', 'Functions', 'Cmdlets', 'DscResources' and 'PowerShellVersion'.</span></span>

<span data-ttu-id="6997d-113">[ID와 제목 간의 차이점은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="6997d-113">[What's the difference between ID and Title?</span></span> <span data-ttu-id="6997d-114">ID는 콘솔에서 사용하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-114">ID is the name you use in the console.</span></span> <span data-ttu-id="6997d-115">제목은 검색 결과에서 패키지 페이지의 맨 위에 표시되는 내용입니다.]</span><span class="sxs-lookup"><span data-stu-id="6997d-115">Title is what is shown at the top of the package page in search results.]</span></span>

## <a name="examples"></a><span data-ttu-id="6997d-116">예</span><span class="sxs-lookup"><span data-stu-id="6997d-116">Examples</span></span>

    ID:"PSReadline"
    id:"AzureRM.Profile"

<span data-ttu-id="6997d-117">ID 필드에 각각 "PSReadline" 또는 "AzureRM.Profile"이 포함된 패키지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-117">finds packages with "PSReadline" or "AzureRM.Profile" in their ID field respectively.</span></span>

    Id:"AzureRM.Profile"

<span data-ttu-id="6997d-118">ID 필드에 "AzureRM.Profile"이 포함된 패키지를 찾는 다른 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-118">is another way to find packages with "AzureRM.Profile" in their ID field.</span></span>

<span data-ttu-id="6997d-119">'Id' 필터는 부분 문자열 일치이므로 다음을 검색하는 경우</span><span class="sxs-lookup"><span data-stu-id="6997d-119">The 'Id' filter is a substring match, so if you search for the following:</span></span>

    Id:"azure"

<span data-ttu-id="6997d-120">'AzureRM.Profile' 및 'Azure.Storage'와 같은 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-120">You'll get results like 'AzureRM.Profile' and 'Azure.Storage'.</span></span>

<span data-ttu-id="6997d-121">또한 단일 필드에서 여러 키워드를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-121">You can also search for multiple keywords in a single field.</span></span> <span data-ttu-id="6997d-122">또는 필드를 섞어서 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-122">Or mix and match fields.</span></span>

    id:azure tags:intellisense
    id:azure id:storage

<span data-ttu-id="6997d-123">구를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-123">And you can perform phrase searches:</span></span>

    id:"azure.storage"


<span data-ttu-id="6997d-124">DSC 태그가 있는 패키지를 모두 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-124">To search all packages with DSC tag.</span></span>

    Tags:"DSC"

<span data-ttu-id="6997d-125">지정된 함수가 있는 패키지를 모두 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-125">To search all packages with the specified function.</span></span>

    Functions:"Update-AzureRM"

<span data-ttu-id="6997d-126">지정된 cmdlet이 있는 패키지를 모두 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-126">To search all packages with the specified cmdlet.</span></span>

    Cmdlets:"Get-AzureRmEnvironment"

<span data-ttu-id="6997d-127">지정된 DSC 리소스 이름이 있는 패키지를 모두 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-127">To search all packages with the specified DSC Resource name.</span></span>

    DscResources:"xArchive"

<span data-ttu-id="6997d-128">지정된 PowerShellVersion이 있는 패키지를 모두 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-128">To search all packages with the specified PowerShellVersion</span></span>

    PowerShellVersion:"5.0"
    PowerShellVersion:"3.0"
    PowerShellVersion:"2.0"


<span data-ttu-id="6997d-129">마지막으로, 지원되지 않는 필드(예: 'commands')를 사용하는 경우 필드가 무시되고 모든 필드가 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-129">Finally, if you use a field we don't support, such as 'commands', we'll just ignore it and search all the fields.</span></span> <span data-ttu-id="6997d-130">따라서 다음 쿼리의 경우</span><span class="sxs-lookup"><span data-stu-id="6997d-130">So the following query</span></span>

    commands:blobs storage

<span data-ttu-id="6997d-131">다음 쿼리와 똑같이 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="6997d-131">Is interpreted exactly the same as this query:</span></span>

    blobs storage
