---
ms.date: 08/14/2018
keywords: powershell,cmdlet
title: PowerShell.exe 명령줄 도움말
ms.assetid: 1ab7b93b-6785-42c6-a1c9-35ff686a958f
ms.openlocfilehash: c7f35511e876e8e5189d8a2b949555603d43f731
ms.sourcegitcommit: 56b9be8503a5a1342c0b85b36f5ba6f57c281b63
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "43133066"
---
# <a name="powershellexe-command-line-help"></a><span data-ttu-id="68a6f-103">PowerShell.exe 명령줄 도움말</span><span class="sxs-lookup"><span data-stu-id="68a6f-103">PowerShell.exe Command-Line Help</span></span>

<span data-ttu-id="68a6f-104">PowerShell.exe를 사용하여 Cmd.exe와 같은 다른 도구의 명령줄에서 PowerShell 세션을 시작하거나, PowerShell 명령줄에서 사용하여 새 세션을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-104">You can use PowerShell.exe to start a PowerShell session from the command line of another tool, such as Cmd.exe, or use it at the PowerShell command line to start a new session.</span></span> <span data-ttu-id="68a6f-105">매개 변수를 사용하여 세션을 사용자 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-105">Use the parameters to customize the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a6f-106">구문</span><span class="sxs-lookup"><span data-stu-id="68a6f-106">Syntax</span></span>

```syntax
PowerShell[.exe]
       [-Command { - | <script-block> [-args <arg-array>]
                     | <string> [<CommandParameters>] } ]
       [-EncodedCommand <Base64EncodedCommand>]
       [-ExecutionPolicy <ExecutionPolicy>]
       [-File <FilePath> [<Args>]]
       [-InputFormat {Text | XML}]
       [-Mta]
       [-NoExit]
       [-NoLogo]
       [-NonInteractive]
       [-NoProfile]
       [-OutputFormat {Text | XML}]
       [-PSConsoleFile <FilePath> | -Version <PowerShell version>]
       [-Sta]
       [-WindowStyle <style>]

PowerShell[.exe] -Help | -? | /?
```

## <a name="parameters"></a><span data-ttu-id="68a6f-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68a6f-107">Parameters</span></span>

### <a name="-encodedcommand-base64encodedcommand"></a><span data-ttu-id="68a6f-108">-EncodedCommand <Base64EncodedCommand></span><span class="sxs-lookup"><span data-stu-id="68a6f-108">-EncodedCommand <Base64EncodedCommand></span></span>

<span data-ttu-id="68a6f-109">명령의 Base 64로 인코드된 문자열 버전을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-109">Accepts a base-64-encoded string version of a command.</span></span> <span data-ttu-id="68a6f-110">이 매개 변수를 사용하여 명령을 큰따옴표 또는 중괄호가 필요한 PowerShell로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-110">Use this parameter to submit commands to PowerShell that require complex quotation marks or curly braces.</span></span>

### <a name="-executionpolicy-executionpolicy"></a><span data-ttu-id="68a6f-111">-ExecutionPolicy <ExecutionPolicy></span><span class="sxs-lookup"><span data-stu-id="68a6f-111">-ExecutionPolicy <ExecutionPolicy></span></span>

<span data-ttu-id="68a6f-112">현재 세션에 대한 기본 실행 정책을 설정하고 $env:PSExecutionPolicyPreference 환경 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-112">Sets the default execution policy for the current session and saves it in the $env:PSExecutionPolicyPreference environment variable.</span></span> <span data-ttu-id="68a6f-113">이 매개 변수는 레지스트리에 설정된 PowerShell 실행 정책을 변경하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-113">This parameter doesn't change the PowerShell execution policy that is set in the registry.</span></span> <span data-ttu-id="68a6f-114">유효한 값 목록을 비롯한 PowerShell 실행 정책에 대한 자세한 내용은 [about_Execution_Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68a6f-114">For information about PowerShell execution policies, including a list of valid values, see [about_Execution_Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

### <a name="-file-filepath-parameters"></a><span data-ttu-id="68a6f-115">-File <FilePath> \[<Parameters>]</span><span class="sxs-lookup"><span data-stu-id="68a6f-115">-File <FilePath> \[<Parameters>]</span></span>

<span data-ttu-id="68a6f-116">스크립트에서 만드는 함수와 변수를 현재 세션에서 사용할 수 있도록 지정한 스크립트를 로컬 범위("dot-sourced")에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-116">Runs the specified script in the local scope ("dot-sourced"), so that the functions and variables that the script creates are available in the current session.</span></span> <span data-ttu-id="68a6f-117">스크립트 파일의 경로와 매개 변수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-117">Enter the script file path and any parameters.</span></span> <span data-ttu-id="68a6f-118">**File**은 명령의 마지막 매개 변수여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-118">**File** must be the last parameter in the command.</span></span> <span data-ttu-id="68a6f-119">**-File** 매개 변수 다음에 입력하는 모든 값은 해당 스크립트에 전달되는 스크립트 파일 경로 및 매개 변수로 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-119">All values typed after the **-File** parameter are interpreted as the script file path and parameters passed to that script.</span></span>

<span data-ttu-id="68a6f-120">스크립트에 전달되는 매개 변수는 리터럴 문자열로 전달됩니다(현재 셸에서 해석한 후).</span><span class="sxs-lookup"><span data-stu-id="68a6f-120">Parameters passed to the script are passed as literal strings (after interpretation by the current shell).</span></span> <span data-ttu-id="68a6f-121">예를 들어 cmd.exe에 있고 환경 변수 값을 전달하려는 경우 cmd.exe 구문 `powershell -File .\test.ps1 -Sample %windir%`를 사용합니다. 이 예제에서 스크립트는 해당 환경 변수 `powershell -File .\test.ps1 -Sample $env:windir` 값이 아니라 리터럴 문자열 `$env:windir`을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-121">For example, if you are in cmd.exe and want to pass an environment variable value, you would use the cmd.exe syntax: `powershell -File .\test.ps1 -Sample %windir%` In this example, the script receives the literal string `$env:windir` and not the value of that environmental variable: `powershell -File .\test.ps1 -Sample $env:windir`</span></span>

### <a name="-inputformat-text--xml"></a><span data-ttu-id="68a6f-122">\-InputFormat {Text | XML}</span><span class="sxs-lookup"><span data-stu-id="68a6f-122">\-InputFormat {Text | XML}</span></span>

<span data-ttu-id="68a6f-123">PowerShell로 전송되는 데이터 형식을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-123">Describes the format of data sent to PowerShell.</span></span> <span data-ttu-id="68a6f-124">유효한 값은 "Text"(텍스트 문자열) 또는 "XML"(직렬화된 CLIXML 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-124">Valid values are "Text" (text strings) or "XML" (serialized CLIXML format).</span></span>

### <a name="-mta"></a><span data-ttu-id="68a6f-125">-Mta</span><span class="sxs-lookup"><span data-stu-id="68a6f-125">-Mta</span></span>

<span data-ttu-id="68a6f-126">다중 스레드 아파트를 사용하여 PowerShell을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-126">Starts PowerShell using a multi-threaded apartment.</span></span> <span data-ttu-id="68a6f-127">이 매개 변수는 PowerShell 3.0에서 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-127">This parameter is introduced in PowerShell 3.0.</span></span> <span data-ttu-id="68a6f-128">PowerShell 3.0에서는 STA(단일 스레드 아파트)가 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-128">In PowerShell 3.0, single-threaded apartment (STA) is the default.</span></span> <span data-ttu-id="68a6f-129">PowerShell 2.0에서는 MTA(다중 스레드 아파트)가 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-129">In PowerShell 2.0, multi-threaded apartment (MTA) is the default.</span></span>

### <a name="-noexit"></a><span data-ttu-id="68a6f-130">-NoExit</span><span class="sxs-lookup"><span data-stu-id="68a6f-130">-NoExit</span></span>

<span data-ttu-id="68a6f-131">시작 명령을 실행한 후 종료하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-131">Doesn't exit after running startup commands.</span></span>

### <a name="-nologo"></a><span data-ttu-id="68a6f-132">-NoLogo</span><span class="sxs-lookup"><span data-stu-id="68a6f-132">-NoLogo</span></span>

<span data-ttu-id="68a6f-133">시작 시 저작권 배너를 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-133">Hides the copyright banner at startup.</span></span>

### <a name="-noninteractive"></a><span data-ttu-id="68a6f-134">-NonInteractive</span><span class="sxs-lookup"><span data-stu-id="68a6f-134">-NonInteractive</span></span>

<span data-ttu-id="68a6f-135">사용자에게 대화형 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-135">Doesn't present an interactive prompt to the user.</span></span>

### <a name="-noprofile"></a><span data-ttu-id="68a6f-136">-NoProfile</span><span class="sxs-lookup"><span data-stu-id="68a6f-136">-NoProfile</span></span>

<span data-ttu-id="68a6f-137">PowerShell 프로필을 로드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-137">Doesn't load the PowerShell profile.</span></span>

### <a name="-outputformat-text--xml"></a><span data-ttu-id="68a6f-138">-OutputFormat {Text | XML}</span><span class="sxs-lookup"><span data-stu-id="68a6f-138">-OutputFormat {Text | XML}</span></span>

<span data-ttu-id="68a6f-139">PowerShell의 출력 형식을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-139">Determines how output from PowerShell is formatted.</span></span> <span data-ttu-id="68a6f-140">유효한 값은 "Text"(텍스트 문자열) 또는 "XML"(직렬화된 CLIXML 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-140">Valid values are "Text" (text strings) or "XML" (serialized CLIXML format).</span></span>

### <a name="-psconsolefile-filepath"></a><span data-ttu-id="68a6f-141">-PSConsoleFile <FilePath></span><span class="sxs-lookup"><span data-stu-id="68a6f-141">-PSConsoleFile <FilePath></span></span>

<span data-ttu-id="68a6f-142">지정된 PowerShell 콘솔 파일을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-142">Loads the specified PowerShell console file.</span></span> <span data-ttu-id="68a6f-143">콘솔 파일의 경로와 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-143">Enter the path and name of the console file.</span></span> <span data-ttu-id="68a6f-144">콘솔 파일을 만들려면 PowerShell에서 [`Export-Console`](/powershell/module/Microsoft.PowerShell.Core/Export-Console) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-144">To create a console file, use the [`Export-Console`](/powershell/module/Microsoft.PowerShell.Core/Export-Console) cmdlet in PowerShell.</span></span>

### <a name="-sta"></a><span data-ttu-id="68a6f-145">-Sta</span><span class="sxs-lookup"><span data-stu-id="68a6f-145">-Sta</span></span>

<span data-ttu-id="68a6f-146">단일 스레드 아파트를 사용하여 PowerShell을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-146">Starts PowerShell using a single-threaded apartment.</span></span> <span data-ttu-id="68a6f-147">PowerShell 3.0에서는 STA(단일 스레드 아파트)가 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-147">In PowerShell 3.0, single-threaded apartment (STA) is the default.</span></span> <span data-ttu-id="68a6f-148">PowerShell 2.0에서는 MTA(다중 스레드 아파트)가 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-148">In PowerShell 2.0, multi-threaded apartment (MTA) is the default.</span></span>

### <a name="-version-powershell-version"></a><span data-ttu-id="68a6f-149">버전 <PowerShell Version></span><span class="sxs-lookup"><span data-stu-id="68a6f-149">-Version <PowerShell Version></span></span>

<span data-ttu-id="68a6f-150">지정된 버전의 PowerShell을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-150">Starts the specified version of PowerShell.</span></span> <span data-ttu-id="68a6f-151">지정한 버전이 시스템에 설치되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-151">The version that you specify must be installed on the system.</span></span> <span data-ttu-id="68a6f-152">컴퓨터에 PowerShell 3.0이 설치되어 있는 경우 유효한 값은 "2.0"과 "3.0"입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-152">If PowerShell 3.0 is installed on the computer, valid values are "2.0" and "3.0".</span></span> <span data-ttu-id="68a6f-153">기본값은 "3.0"입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-153">The default value is "3.0".</span></span>

<span data-ttu-id="68a6f-154">PowerShell 3.0이 설치되지 않은 경우 유효한 값은 "2.0"뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-154">If PowerShell 3.0 isn't installed, the only valid value is "2.0".</span></span> <span data-ttu-id="68a6f-155">다른 값은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-155">Other values are ignored.</span></span>

<span data-ttu-id="68a6f-156">자세한 내용은 [Windows PowerShell 설치](../../setup/installing-windows-powershell.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68a6f-156">For more information, see [Installing Windows PowerShell](../../setup/installing-windows-powershell.md).</span></span>

### <a name="-windowstyle-window-style"></a><span data-ttu-id="68a6f-157">-WindowStyle <Window style></span><span class="sxs-lookup"><span data-stu-id="68a6f-157">-WindowStyle <Window style></span></span>

<span data-ttu-id="68a6f-158">세션에 대한 창 스타일을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-158">Sets the window style for the session.</span></span> <span data-ttu-id="68a6f-159">유효한 값은 Normal, Minimized, Maximized 및 Hidden입니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-159">Valid values are Normal, Minimized, Maximized, and Hidden.</span></span>

### <a name="-command"></a><span data-ttu-id="68a6f-160">-Command</span><span class="sxs-lookup"><span data-stu-id="68a6f-160">-Command</span></span>

<span data-ttu-id="68a6f-161">지정된 명령(및 매개 변수)을 PowerShell 명령 프롬프트에서 입력된 것처럼 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-161">Executes the specified commands (with any parameters) as though they were typed at the PowerShell command prompt.</span></span> <span data-ttu-id="68a6f-162">`-NoExit` 매개 변수가 지정되지 않은 경우, 실행 후에 PowerShell은 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-162">After execution, PowerShell exits unless the `-NoExit` parameter is specified.</span></span>
<span data-ttu-id="68a6f-163">`-Command` 다음의 모든 텍스트는 PowerShell에 단일 명령줄로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-163">Any text after `-Command` is sent as a single command line to PowerShell.</span></span> <span data-ttu-id="68a6f-164">이것은 `-File`이 스크립트에 전송된 매개 변수를 처리하는 방식과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-164">This is different from how `-File` handles parameters sent to a script.</span></span>

<span data-ttu-id="68a6f-165">명령의 값은 "-", 문자열</span><span class="sxs-lookup"><span data-stu-id="68a6f-165">The value of Command can be "-", a string.</span></span> <span data-ttu-id="68a6f-166">또는 스크립트 블록일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-166">or a script block.</span></span> <span data-ttu-id="68a6f-167">명령의 값이 "-"인 경우 표준 입력에서 명령 텍스트를 읽어옵니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-167">If the value of Command is "-", the command text is read from standard input.</span></span>

<span data-ttu-id="68a6f-168">스크립트 블록은 중괄호({})로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-168">Script blocks must be enclosed in braces ({}).</span></span> <span data-ttu-id="68a6f-169">PowerShell에서 PowerShell.exe를 실행하는 경우에만 스크립트 블록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-169">You can specify a script block only when running PowerShell.exe in PowerShell.</span></span> <span data-ttu-id="68a6f-170">스크립트의 결과는 라이브 개체가 아니라 역직렬화된 XML 개체로 부모 셸에 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-170">The results of the script are returned to the parent shell as deserialized XML objects, not live objects.</span></span>

<span data-ttu-id="68a6f-171">명령의 값이 문자열인 경우 명령 뒤에 입력한 문자는 모두 명령 인수로 해석되므로 **Command**가 명령의 마지막 매개 변수여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-171">If the value of Command is a string, **Command** must be the last parameter in the command, because any characters typed after the command are interpreted as the command arguments.</span></span>

<span data-ttu-id="68a6f-172">PowerShell 명령을 실행하는 문자열을 작성하려면 다음 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-172">To write a string that runs a PowerShell command, use the format:</span></span>

```powershell
"& {<command>}"
```

<span data-ttu-id="68a6f-173">따옴표는 문자열을 나타내고 호출 연산자(&)는 명령이 실행되게 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-173">The quotation marks indicate a string and the invoke operator (&) causes the command to be executed.</span></span>

### <a name="-help---"></a><span data-ttu-id="68a6f-174">-Help, -?, /?</span><span class="sxs-lookup"><span data-stu-id="68a6f-174">-Help, -?, /?</span></span>

<span data-ttu-id="68a6f-175">powershell.exe의 구문을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-175">Shows the syntax of powershell.exe.</span></span> <span data-ttu-id="68a6f-176">PowerShell에서 PowerShell.exe 명령을 입력하는 경우 명령 매개 변수 앞에 슬래시(/)가 아니라 하이픈(-)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-176">If you are typing a PowerShell.exe command in PowerShell, prepend the command parameters with a hyphen (-), not a forward slash (/).</span></span> <span data-ttu-id="68a6f-177">Cmd.exe에서는 하이픈 또는 슬래시를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-177">You can use either a hyphen or forward slash in Cmd.exe.</span></span>

> [!NOTE]
> <span data-ttu-id="68a6f-178">문제 해결 참고: PowerShell 2.0에서 Windows PowerShell 콘솔을 통해 일부 프로그램을 시작하면 실패하고 LastExitCode 0xc0000142가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a6f-178">Troubleshooting Note: In PowerShell 2.0, starting some programs in the Windows PowerShell console fails with a LastExitCode of 0xc0000142.</span></span>

## <a name="examples"></a><span data-ttu-id="68a6f-179">예제</span><span class="sxs-lookup"><span data-stu-id="68a6f-179">EXAMPLES</span></span>

```powershell
# Create a new PowerShell session and load a saved console file
PowerShell -PSConsoleFile sqlsnapin.psc1

# Create a new PowerShell V2 session with text input, XML output, and no logo
PowerShell -Version 2.0 -NoLogo -InputFormat text -OutputFormat XML

# Execute a PowerShell Command in a session
PowerShell -Command "Get-EventLog -LogName security"

# Run a script block in a session
PowerShell -Command {Get-EventLog -LogName security}

# An alternate way to run a command in a new session
PowerShell -Command "& {Get-EventLog -LogName security}"

# To use the -EncodedCommand parameter:
$command = "dir 'c:\program files' "
$bytes = [System.Text.Encoding]::Unicode.GetBytes($command)
$encodedCommand = [Convert]::ToBase64String($bytes)
powershell.exe -encodedCommand $encodedCommand
```
