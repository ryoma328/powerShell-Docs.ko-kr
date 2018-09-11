---
ms.date: 08/14/2018
keywords: powershell,cmdlet
title: Windows PowerShell ISE 소개
ms.openlocfilehash: d27a0eb594d7271121cee59f38d096995cc98648
ms.sourcegitcommit: 56b9be8503a5a1342c0b85b36f5ba6f57c281b63
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "43133139"
---
# <a name="introducing-the-windows-powershell-ise"></a><span data-ttu-id="fb891-103">Windows PowerShell ISE 소개</span><span class="sxs-lookup"><span data-stu-id="fb891-103">Introducing the Windows PowerShell ISE</span></span>

<span data-ttu-id="fb891-104">Windows PowerShell ISE(통합 스크립팅 환경)는 Windows PowerShell의 호스트 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-104">The Windows PowerShell Integrated Scripting Environment (ISE) is a host application for Windows PowerShell.</span></span> <span data-ttu-id="fb891-105">Windows PowerShell ISE에서는 단일 Windows 기반 그래픽 사용자 인터페이스에서 명령을 실행하고, 스크립트를 작성, 테스트 및 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-105">In Windows PowerShell ISE, you can run commands and write, test, and debug scripts in a single Windows-based graphic user interface.</span></span> <span data-ttu-id="fb891-106">이 인터페이스는 여러 줄 편집, 탭 완성, 구문 색 지정, 선택적 실행, 상황에 맞는 도움말 및 오른쪽에서 왼쪽으로 쓰는 언어 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-106">The interface provides multiline editing, tab completion, syntax coloring, selective execution, context-sensitive help, and support for right-to-left languages.</span></span> <span data-ttu-id="fb891-107">메뉴 항목 및 바로 가기 키가 Windows PowerShell 콘솔에서 수행하는 것과 동일한 많은 작업에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-107">Menu items and keyboard shortcuts are mapped to many of the same tasks that you would do in the Windows PowerShell console.</span></span> <span data-ttu-id="fb891-108">예를 들어, Windows PowerShell ISE에서 스크립트를 디버그할 때 코드 줄을 마우스 오른쪽 단추로 클릭하여 중단점을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-108">For example, when you debug a script in the Windows PowerShell ISE, you can right-click on a line of code to set a breakpoint.</span></span>

<span data-ttu-id="fb891-109">Windows PowerShell ISE에서 이러한 기능을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-109">Try these features in Windows PowerShell ISE.</span></span>

- <span data-ttu-id="fb891-110">여러 줄 편집: 명령 창에서 현재 줄 아래에 빈 줄을 삽입하려면 Shift+Enter를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-110">Multiline editing: To insert a blank line under the current line in the Command pane, press SHIFT+ENTER.</span></span>
- <span data-ttu-id="fb891-111">선택적 실행: 스크립트의 일부를 실행하려면 실행할 텍스트를 선택한 다음 **스크립트 실행** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-111">Selective execution: To run part of a script, select the text you want to run, and then click the **Run Script** button.</span></span> <span data-ttu-id="fb891-112">또는 F5 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-112">Or, press F5.</span></span>
- <span data-ttu-id="fb891-113">상황에 맞는 도움말: **Invoke-Item**을 입력하고 F1 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-113">Context-sensitive help: Type **Invoke-Item**, and then press F1.</span></span> <span data-ttu-id="fb891-114">도움말 파일이 **Invoke-Item** cmdlet에 대한 문서로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-114">The Help file opens to the article for the **Invoke-Item** cmdlet.</span></span>

<span data-ttu-id="fb891-115">Windows PowerShell ISE를 사용하여 해당 모양의 일부 측면을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-115">The Windows PowerShell ISE lets you customize some aspects of its appearance.</span></span> <span data-ttu-id="fb891-116">또한 자체 Windows PowerShell 프로필 스크립트도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-116">It also has its own Windows PowerShell profile script.</span></span>

## <a name="to-start-the-windows-powershell-ise"></a><span data-ttu-id="fb891-117">Windows PowerShell ISE를 시작하려면</span><span class="sxs-lookup"><span data-stu-id="fb891-117">To start the Windows PowerShell ISE</span></span>

<span data-ttu-id="fb891-118">**시작**을 클릭하고 **Windows PowerShell**을 선택한 후 고 **Windows PowerShell ISE**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-118">Click **Start**, select **Windows PowerShell**, and then click **Windows PowerShell ISE**.</span></span>
<span data-ttu-id="fb891-119">또는 임의 명령 셸이나 실행 상자에 `powershell_ise.exe`를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-119">Alternately, you can type `powershell_ise.exe` in any command shell or in the Run box.</span></span>

## <a name="to-get-help-in-the-windows-powershell-ise"></a><span data-ttu-id="fb891-120">Windows PowerShell ISE에서 도움말을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="fb891-120">To get Help in the Windows PowerShell ISE</span></span>

<span data-ttu-id="fb891-121">**도움말** 메뉴에서 **Windows PowerShell 도움말**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-121">On the **Help** menu, click **Windows PowerShell Help**.</span></span> <span data-ttu-id="fb891-122">또는 F1 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-122">Or, press F1.</span></span> <span data-ttu-id="fb891-123">열린 파일에는 Get-Help cmdlet에서 사용 가능한 모든 도움말을 비롯하여 Windows PowerShell ISE 및 Windows PowerShell이 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb891-123">The file that opens describes Windows PowerShell ISE and Windows PowerShell, including all of the help available from the Get-Help cmdlet.</span></span>