---
ms.date: 08/27/2018
keywords: powershell,cmdlet
title: 변수를 사용하여 개체 저장
ms.assetid: b1688d73-c173-491e-9ba6-6d0c1cc852de
ms.openlocfilehash: f4254199facb914c68a487b281b30070c35550a1
ms.sourcegitcommit: c170a1608d20d3c925d79c35fa208f650d014146
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2018
ms.locfileid: "43353221"
---
# <a name="using-variables-to-store-objects"></a><span data-ttu-id="34284-103">변수를 사용하여 개체 저장</span><span class="sxs-lookup"><span data-stu-id="34284-103">Using variables to store objects</span></span>

<span data-ttu-id="34284-104">PowerShell에서는 개체에 대한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-104">PowerShell works with objects.</span></span> <span data-ttu-id="34284-105">PowerShell을 사용하면 변수라고 하는 명명된 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-105">PowerShell lets you create named objects known as variables.</span></span>
<span data-ttu-id="34284-106">변수 이름에는 밑줄 문자와 영숫자 문자가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-106">Variables names can include the underscore character can any alphanumeric characters.</span></span> <span data-ttu-id="34284-107">PowerShell에서 사용하는 경우는 변수는 항상 \$ 문자와 변수 이름을 차례로 입력하여 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-107">When used in PowerShell, a variable is always specified using the \$ character followed by variable name.</span></span>

## <a name="creating-a-variable"></a><span data-ttu-id="34284-108">변수 만들기</span><span class="sxs-lookup"><span data-stu-id="34284-108">Creating a variable</span></span>

<span data-ttu-id="34284-109">변수를 만들려면 다음과 같이 유효한 변수 이름을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-109">You can create a variable by typing a valid variable name:</span></span>

```
PS> $loc
PS>
```

<span data-ttu-id="34284-110">이 예제에서는 `$loc`에 값이 없기 때문에 아무 결과도 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-110">This example returns no result because `$loc` doesn't have a value.</span></span> <span data-ttu-id="34284-111">동일한 단계에서 변수를 만드는 작업과 변수에 값을 할당하는 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-111">You can create a variable and assign it a value in the same step.</span></span> <span data-ttu-id="34284-112">PowerShell은 변수가 없는 경우에만 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34284-112">PowerShell only creates the variable if it doesn't exist.</span></span>
<span data-ttu-id="34284-113">그렇지 않으면 지정된 값을 기존 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-113">Otherwise, it assigns the specified value to the existing variable.</span></span> <span data-ttu-id="34284-114">다음 예제에서는 현재 위치를 변수 `$loc`에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-114">The following example stores the current location in the variable `$loc`:</span></span>

```powershell
$loc = Get-Location
```

<span data-ttu-id="34284-115">이 명령을 입력할 때 PowerShell은 출력을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-115">PowerShell displays no output when you type this command.</span></span> <span data-ttu-id="34284-116">PowerShell은 ‘Get-location’의 출력을 `$loc`로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="34284-116">PowerShell sends the output of 'Get-Location' to `$loc`.</span></span> <span data-ttu-id="34284-117">PowerShell에서 할당 또는 리디렉션되지 않는 데이터는 화면으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="34284-117">In PowerShell, data that isn't assigned or redirected is sent to the screen.</span></span> <span data-ttu-id="34284-118">`$loc`를 입력하면 현재 위치가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34284-118">Typing `$loc` shows your current location:</span></span>

```
PS> $loc

Path
----
C:\temp
```

<span data-ttu-id="34284-119">`Get-Member`를 사용하여 변수의 내용에 대한 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-119">You can use `Get-Member` to display information about the contents of variables.</span></span> <span data-ttu-id="34284-120">`Get-Member`는 `Get-Location`의 출력과 마찬가지로 `$loc`가 **PathInfo** 개체임을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34284-120">`Get-Member` shows you that `$loc` is a **PathInfo** object, just like the output from `Get-Location`:</span></span>

```powershell
PS> $loc | Get-Member -MemberType Property

   TypeName: System.Management.Automation.PathInfo

Name         MemberType Definition
----         ---------- ----------
Drive        Property   System.Management.Automation.PSDriveInfo Drive {get;}
Path         Property   System.String Path {get;}
Provider     Property   System.Management.Automation.ProviderInfo Provider {...
ProviderPath Property   System.String ProviderPath {get;}
```

## <a name="manipulating-variables"></a><span data-ttu-id="34284-121">변수 조작</span><span class="sxs-lookup"><span data-stu-id="34284-121">Manipulating variables</span></span>

<span data-ttu-id="34284-122">PowerShell에는 변수를 조작할 수 있는 여러 명령이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-122">PowerShell provides several commands to manipulate variables.</span></span> <span data-ttu-id="34284-123">다음과 같이 입력하면 이러한 명령의 전체 목록을 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-123">You can see a complete listing in a readable form by typing:</span></span>

```powershell
Get-Command -Noun Variable | Format-Table -Property Name,Definition -AutoSize -Wrap
```

<span data-ttu-id="34284-124">PowerShell은 또한 여러 시스템 정의 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34284-124">PowerShell also creates several system-defined variables.</span></span> <span data-ttu-id="34284-125">`Remove-Variable` cmdlet을 사용하여 현재 세션에서 PowerShell에 의해 제어되지 않는 변수를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-125">You can use the `Remove-Variable` cmdlet to remove variables, which are not controlled by PowerShell, from the current session.</span></span> <span data-ttu-id="34284-126">다음 명령을 입력하면 모든 변수를 지울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-126">Type the following command to clear all variables:</span></span>

```powershell
Remove-Variable -Name * -Force -ErrorAction SilentlyContinue
```

<span data-ttu-id="34284-127">`Get-Variable` cmdlet은 이전 명령을 실행한 후에 PowerShell 시스템 변수를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-127">After running the previous command, the `Get-Variable` cmdlet shows the PowerShell system variables.</span></span>

<span data-ttu-id="34284-128">또한 PowerShell은 변수 드라이브도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34284-128">PowerShell also creates a variable drive.</span></span> <span data-ttu-id="34284-129">변수 드라이브를 사용하는 모든 PowerShell 변수를 표시하려면 다음 예제를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-129">Use the following example to display all PowerShell variables using the variable drive:</span></span>

```powershell
Get-ChildItem variable:
```

## <a name="using-cmdexe-variables"></a><span data-ttu-id="34284-130">cmd.exe 변수 사용</span><span class="sxs-lookup"><span data-stu-id="34284-130">Using cmd.exe variables</span></span>

<span data-ttu-id="34284-131">PowerShell에서는 모든 Windows 프로세스(**cmd.exe** 포함)에서 사용할 수 있는 동일한 환경 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-131">PowerShell can use the same environment variables available to any Windows process, including **cmd.exe**.</span></span> <span data-ttu-id="34284-132">이러한 변수는 `env:`라는 드라이브를 통해 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34284-132">These variables are exposed through a drive named `env:`.</span></span> <span data-ttu-id="34284-133">다음 명령을 입력하면 이러한 변수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-133">You can view these variables by typing the following command:</span></span>

```powershell
Get-ChildItem env:
```

<span data-ttu-id="34284-134">표준 `*-Variable` cmdlet은 환경 변수를 사용하도록 디자인되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-134">The standard `*-Variable` cmdlets aren't designed to work with environment variables.</span></span> <span data-ttu-id="34284-135">환경 변수는 `env:` 드라이브 접두사를 사용하여 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-135">Environment variables are accessed using the `env:` drive prefix.</span></span> <span data-ttu-id="34284-136">예를 들어 **cmd.exe**의 **% SystemRoot %** 변수에는 운영 체제의 루트 디렉터리 이름이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="34284-136">For example, the **%SystemRoot%** variable in **cmd.exe** contains the operating system's root directory name.</span></span> <span data-ttu-id="34284-137">PowerShell에서 `$env:SystemRoot`를 사용하여 동일한 값에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="34284-137">In PowerShell, you use `$env:SystemRoot` to access the same value.</span></span>

```
PS> $env:SystemRoot
C:\WINDOWS
```

<span data-ttu-id="34284-138">또한 PowerShell에서 환경 변수를 만들고 수정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34284-138">You can also create and modify environment variables from within PowerShell.</span></span> <span data-ttu-id="34284-139">PowerShell의 환경 변수는 운영 체제에서 사용되는 환경 변수에 대해 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="34284-139">Environment variables in PowerShell follow the same rules for environment variables used elsewhere in the operating system.</span></span> <span data-ttu-id="34284-140">다음 예제는 새 환경 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34284-140">The following example creates a new environment variable:</span></span>

```powershell
$env:LIB_PATH='/usr/local/lib'
```

<span data-ttu-id="34284-141">필수는 아니지만, 환경 변수 이름을 모두 대문자로 지정하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="34284-141">Though not required, is it common for environment variable names to use all uppercase letters.</span></span>