---
ms.date: 06/05/2017
keywords: powershell,cmdlet
title: Windows PowerShell SDK 설치
ms.assetid: c3636b45-61aa-4720-85f0-58312c4fc8f9
ms.openlocfilehash: fa876bac0c1afac24f93d11dd2e7ecfb1165cf5f
ms.sourcegitcommit: 8b076ebde7ef971d7465bab834a3c2a32471ef6f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37893541"
---
# <a name="installing-the-windows-powershell-sdk"></a><span data-ttu-id="090b4-103">Windows PowerShell SDK 설치</span><span class="sxs-lookup"><span data-stu-id="090b4-103">Installing the Windows PowerShell SDK</span></span>

<span data-ttu-id="090b4-104">다음 항목에서는 여러 버전의 Windows에 PowerShell SDK를 설치하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-104">The following topic describes how to install the PowerShell SDK on different versions of Windows.</span></span>

## <a name="installing-windows-powershell-30-sdk-for-windows-8-and-windows-server-2012"></a><span data-ttu-id="090b4-105">Windows 8 및 Windows Server 2012용 Windows PowerShell 3.0 SDK 설치</span><span class="sxs-lookup"><span data-stu-id="090b4-105">Installing Windows PowerShell 3.0 SDK for Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="090b4-106">Windows PowerShell 3.0은 Windows 8 및 Windows Server 2012와 함께 자동으로 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-106">Windows PowerShell 3.0 is automatically installed with Windows 8 and Windows Server 2012.</span></span>
<span data-ttu-id="090b4-107">또한 Windows 8 SDK의 일부로써 Windows PowerShell 3.0의 참조 어셈블리를 다운로드하고 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-107">In addition, you can download and install the reference assemblies for Windows PowerShell 3.0 as part of the Windows 8 SDK.</span></span>
<span data-ttu-id="090b4-108">이러한 어셈블리를 사용하여 Windows PowerShell 3.0에 대한 cmdlet, 공급자 및 호스트 프로그램을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-108">These assemblies allow you to write cmdlets, providers, and host programs for Windows PowerShell 3.0.</span></span>
<span data-ttu-id="090b4-109">Windows 8용 Windows SDK를 설치하면 Windows PowerShell 어셈블리가 참조 어셈블리 폴더(`\Program Files (x86)\Reference Assemblies\Microsoft\WindowsPowerShell\3.0`)에 자동으로 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-109">When you install the Windows SDK for Windows 8, the Windows PowerShell assemblies are automatically installed in the reference assembly folder, in `\Program Files (x86)\Reference Assemblies\Microsoft\WindowsPowerShell\3.0`.</span></span>
<span data-ttu-id="090b4-110">자세한 내용은 [Windows 8 SDK 다운로드 사이트](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="090b4-110">For more information, see the [Windows 8 SDK download site](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive).</span></span>
<span data-ttu-id="090b4-111">Windows PowerShell 코드 샘플은 개발자 센터에서도 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-111">Windows PowerShell code samples are also available on the Development Center.</span></span>
<span data-ttu-id="090b4-112">자세한 내용은 [개발자 센터 사이트](https://code.msdn.microsoft.com:443/windowsdesktop/)에서 데스크톱 코드 샘플 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="090b4-112">For more information, see the Desktop code sample page on the [Dev center site](https://code.msdn.microsoft.com:443/windowsdesktop/).</span></span>

<span data-ttu-id="090b4-113">또한 Windows PowerShell 3.0은 다수의 코드 샘플이 포함된 이전 버전인 Windows PowerShell 2.0 SDK와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-113">In addition, Windows PowerShell 3.0 is backwards-compatible with the Windows PowerShell 2.0 SDK, which includes a number of code samples.</span></span>
<span data-ttu-id="090b4-114">Windows PowerShell 2.0 SDK를 다운로드하는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="090b4-114">For more information on how to download the Windows PowerShell 2.0 SDK, see below.</span></span>
<span data-ttu-id="090b4-115">(2.0 코드 샘플은 Windows 8 및 Windows PowerShell 3.0과 호환되지만 Windows 8 플랫폼에 Windows PowerShell 2.0을 설치할 수 없습니다.)</span><span class="sxs-lookup"><span data-stu-id="090b4-115">(Note that while the 2.0 code samples are compatible with Windows 8 and Windows PowerShell 3.0, you cannot install Windows PowerShell 2.0 on a Windows 8 platform.)</span></span>

## <a name="installing-windows-powershell-30-sdk-for-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="090b4-116">Windows 7 및 Windows Server 2008 R2용 Windows PowerShell 3.0 SDK 설치</span><span class="sxs-lookup"><span data-stu-id="090b4-116">Installing Windows PowerShell 3.0 SDK for Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="090b4-117">Windows 7 및 Windows Server 2008 R2는 PowerShell 2.0을 자동으로 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-117">Windows 7 and Windows Server 2008 R2 automatically have PowerShell 2.0 installed.</span></span>
<span data-ttu-id="090b4-118">또한 이러한 시스템에 PowerShell 3.0을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-118">In addition, you can install PowerShell 3.0 on these systems.</span></span>
<span data-ttu-id="090b4-119">자세한 내용은 [Windows PowerShell 설치](Installing-Windows-PowerShell.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="090b4-119">(For more information, see [Installing Windows PowerShell](Installing-Windows-PowerShell.md).).</span></span>
<span data-ttu-id="090b4-120">위에서 설명한 대로, Windows 7 및 Windows Server 2008 R2에서도 Windows 8 SDK를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-120">As described above, you can also install the Windows 8 SDK on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="installing-windows-powershell-20-sdk-for-windows-7-vista-xp-server-2003-and-server-2008"></a><span data-ttu-id="090b4-121">Windows 7, Vista, XP, Server 2003 및 Server 2008용 Windows PowerShell 2.0 SDK 설치</span><span class="sxs-lookup"><span data-stu-id="090b4-121">Installing Windows PowerShell 2.0 SDK for Windows 7, Vista, XP, Server 2003, and Server 2008</span></span>

<span data-ttu-id="090b4-122">Windows PowerShell 2.0 SDK는 cmdlet, 공급자 및 호스팅 응용 프로그램을 작성하는 데 필요한 참조 어셈블리를 제공하고 코드 작성을 시작할 때 시작 지점으로 사용할 수 있는 C# 샘플 코드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-122">The Windows PowerShell 2.0 SDK provides the reference assemblies needed to write cmdlets, providers, and hosting applications, and it provides C# sample code that can be used as the starting point when you begin writing code.</span></span>

<span data-ttu-id="090b4-123">이 SDK를 설치하려면 [Windows PowerShell 2.0 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=2560)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="090b4-123">To install this SDK, see [Windows PowerShell 2.0 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=2560).</span></span>

## <a name="reference-assemblies"></a><span data-ttu-id="090b4-124">참조 어셈블리</span><span class="sxs-lookup"><span data-stu-id="090b4-124">Reference assemblies</span></span>

<span data-ttu-id="090b4-125">참조 어셈블리는 기본적으로 다음 위치에 설치됩니다. `c:\Program Files\Reference Assemblies\Microsoft\WindowsPowerShell\V1.0`</span><span class="sxs-lookup"><span data-stu-id="090b4-125">Reference assemblies are installed in the following location by default: `c:\Program Files\Reference Assemblies\Microsoft\WindowsPowerShell\V1.0`.</span></span>

> [!NOTE] 
> <span data-ttu-id="090b4-126">Windows PowerShell 2.0 어셈블리에 대해 컴파일된 코드는 Windows PowerShell 1.0 설치에 로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-126">Code that is compiled against the Windows PowerShell 2.0 assemblies cannot be loaded into Windows PowerShell 1.0 installations.</span></span>
> <span data-ttu-id="090b4-127">그러나 Windows PowerShell 1.0 어셈블리에 대해 컴파일되는 코드는 Windows PowerShell 2.0 설치에 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-127">However, code that is compiled against the Windows PowerShell 1.0 assemblies can be loaded into Windows PowerShell 2.0 installations.</span></span>

## <a name="samples"></a><span data-ttu-id="090b4-128">샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-128">Samples</span></span>

<span data-ttu-id="090b4-129">코드 샘플은 기본적으로 다음 위치에 설치됩니다. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\WindowsPowerShell\`</span><span class="sxs-lookup"><span data-stu-id="090b4-129">Code samples are installed in the following location by default: `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\WindowsPowerShell\`.</span></span>

<span data-ttu-id="090b4-130">다음 섹션에서는 각 샘플의 용도에 대해 간략하게 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-130">The following sections provide a brief description of what each sample does.</span></span>

## <a name="cmdlet-samples"></a><span data-ttu-id="090b4-131">Cmdlet 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-131">Cmdlet samples</span></span>

### <a name="getprocesssample01"></a><span data-ttu-id="090b4-132">GetProcessSample01</span><span class="sxs-lookup"><span data-stu-id="090b4-132">GetProcessSample01</span></span>

<span data-ttu-id="090b4-133">로컬 컴퓨터에 있는 모든 프로세스를 가져오는 간단한 cmdlet을 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-133">Shows how to write a simple cmdlet that gets all the processes on the local computer.</span></span>

### <a name="getprocesssample02"></a><span data-ttu-id="090b4-134">GetProcessSample02</span><span class="sxs-lookup"><span data-stu-id="090b4-134">GetProcessSample02</span></span>

<span data-ttu-id="090b4-135">cmdlet에 매개 변수를 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-135">Shows how to add parameters to the cmdlet.</span></span>
<span data-ttu-id="090b4-136">cmdlet은 하나 이상의 프로세스 이름을 사용하고 일치하는 프로세스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-136">The cmdlet takes one or more process names and returns the matching processes.</span></span>

### <a name="getprocesssample03"></a><span data-ttu-id="090b4-137">GetProcessSample03</span><span class="sxs-lookup"><span data-stu-id="090b4-137">GetProcessSample03</span></span>

<span data-ttu-id="090b4-138">파이프라인의 입력을 허용하는 매개 변수를 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-138">Shows how to add parameters that accept input from the pipeline.</span></span>

### <a name="getprocesssample04"></a><span data-ttu-id="090b4-139">GetProcessSample04</span><span class="sxs-lookup"><span data-stu-id="090b4-139">GetProcessSample04</span></span>

<span data-ttu-id="090b4-140">종료되지 않는 오류를 처리하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-140">Shows how to handle nonterminating errors.</span></span>

### <a name="getprocesssample05"></a><span data-ttu-id="090b4-141">GetProcessSample05</span><span class="sxs-lookup"><span data-stu-id="090b4-141">GetProcessSample05</span></span>

<span data-ttu-id="090b4-142">지정한 프로세스 목록을 표시하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-142">Shows how to display a list of specified processes.</span></span>

### <a name="selectobject"></a><span data-ttu-id="090b4-143">SelectObject</span><span class="sxs-lookup"><span data-stu-id="090b4-143">SelectObject</span></span>

<span data-ttu-id="090b4-144">특정 개체만 선택하는 필터를 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-144">Shows how to write a filter to select only certain objects.</span></span>

### <a name="selectstring"></a><span data-ttu-id="090b4-145">SelectString</span><span class="sxs-lookup"><span data-stu-id="090b4-145">SelectString</span></span>

<span data-ttu-id="090b4-146">파일에서 지정한 패턴을 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-146">Shows how to search files for specified patterns.</span></span>

### <a name="stopprocesssample01"></a><span data-ttu-id="090b4-147">StopProcessSample01</span><span class="sxs-lookup"><span data-stu-id="090b4-147">StopProcessSample01</span></span>

<span data-ttu-id="090b4-148">*PassThru* 매개 변수를 구현하는 방법과 [ShouldProcess](/dotnet/api/system.management.automation.cmdlet.shouldprocess) 및 [ShouldContinue](/dotnet/api/system.management.automation.cmdlet.shouldcontinue) 메서드를 호출하여 사용자 피드백을 요청하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-148">Shows how to implement a *PassThru* parameter, and how to request user feedback by calls to the [ShouldProcess](/dotnet/api/system.management.automation.cmdlet.shouldprocess) and [ShouldContinue](/dotnet/api/system.management.automation.cmdlet.shouldcontinue) methods.</span></span>
<span data-ttu-id="090b4-149">사용자는 cmdlet에서 강제로 개체를 반환하려는 경우 *PassThru* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-149">Users specify the *PassThru* parameter when they want to force the cmdlet to return an object,</span></span>

### <a name="stopprocesssample02"></a><span data-ttu-id="090b4-150">StopProcessSample02</span><span class="sxs-lookup"><span data-stu-id="090b4-150">StopProcessSample02</span></span>

<span data-ttu-id="090b4-151">특정 프로세스를 중지하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-151">Shows how to stop a specific process.</span></span>

### <a name="stopprocesssample03"></a><span data-ttu-id="090b4-152">StopProcessSample03</span><span class="sxs-lookup"><span data-stu-id="090b4-152">StopProcessSample03</span></span>

<span data-ttu-id="090b4-153">매개 변수의 별칭을 선언하는 방법과 와일드카드를 지원하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-153">Shows how to declare aliases for parameters and how to support wildcards.</span></span>

### <a name="stopprocesssample04"></a><span data-ttu-id="090b4-154">StopProcessSample04</span><span class="sxs-lookup"><span data-stu-id="090b4-154">StopProcessSample04</span></span>

<span data-ttu-id="090b4-155">매개 변수 집합을 선언하는 방법 및 cmdlet이 입력으로 사용하는 개체를 선언하는 방법, 그리고 사용할 기본 매개 변수 집합을 지정하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-155">Shows how to declare parameter sets, the object that the cmdlet takes as input, and how to specify the default parameter set to use.</span></span>

## <a name="remoting-samples"></a><span data-ttu-id="090b4-156">원격 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-156">Remoting samples</span></span>

### <a name="remoterunspace01"></a><span data-ttu-id="090b4-157">RemoteRunspace01</span><span class="sxs-lookup"><span data-stu-id="090b4-157">RemoteRunspace01</span></span>

<span data-ttu-id="090b4-158">원격 연결을 설정하는 데 사용되는 원격 runspace를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-158">Shows how to create a remote runspace that is used to establish a remote connection.</span></span>

### <a name="remoterunspacepool01"></a><span data-ttu-id="090b4-159">RemoteRunspacePool01</span><span class="sxs-lookup"><span data-stu-id="090b4-159">RemoteRunspacePool01</span></span>

<span data-ttu-id="090b4-160">원격 runspace 풀을 생성하는 방법과 이 풀을 사용하여 여러 명령을 동시에 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-160">Shows how to construct a remote runspace pool and how to run multiple commands concurrently by using this pool.</span></span>

### <a name="serialization01"></a><span data-ttu-id="090b4-161">Serialization01</span><span class="sxs-lookup"><span data-stu-id="090b4-161">Serialization01</span></span>

<span data-ttu-id="090b4-162">기존 .NET 클래스를 살펴보고 이 클래스의 선택한 공용 속성 정보가 직렬화/역직렬화에서 유지되는지 확인하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-162">Shows how to look at an existing .NET class and make sure that information from selected public properties of this class is preserved across serialization/deserialization.</span></span>

### <a name="serialization02"></a><span data-ttu-id="090b4-163">Serialization02</span><span class="sxs-lookup"><span data-stu-id="090b4-163">Serialization02</span></span>

<span data-ttu-id="090b4-164">기존 .NET 클래스를 살펴보고 이 클래스 인스턴스의 정보가 클래스의 공용 속성에 제공되지 않는 경우, 해당 정보가 직렬화/역직렬화에서 유지되는지 확인하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-164">Shows how to look at an existing .NET class and make sure that information from instance of this class is preserved across serialization/deserialization when the information is not available in public properties of the class.</span></span>

### <a name="serialization03"></a><span data-ttu-id="090b4-165">Serialization03</span><span class="sxs-lookup"><span data-stu-id="090b4-165">Serialization03</span></span>

<span data-ttu-id="090b4-166">기존 .NET 클래스를 살펴보고 이 클래스 및 파생 클래스의 인스턴스가 라이브 .NET 개체로 역직렬화(리하이드레이션)되는지 확인하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-166">Shows how to look at an existing .NET class and make sure that instances of this class and of derived classes are deserialized (rehydrated) into live .NET objects.</span></span>

## <a name="event-samples"></a><span data-ttu-id="090b4-167">이벤트 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-167">Event samples</span></span>

### <a name="event01"></a><span data-ttu-id="090b4-168">Event01</span><span class="sxs-lookup"><span data-stu-id="090b4-168">Event01</span></span>

<span data-ttu-id="090b4-169">ObjectEventRegistrationBase에서 파생하여 이벤트 등록용 cmdlet을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-169">Shows how to create a cmdlet for event registration by deriving from ObjectEventRegistrationBase.</span></span>

### <a name="event02"></a><span data-ttu-id="090b4-170">Event02</span><span class="sxs-lookup"><span data-stu-id="090b4-170">Event02</span></span>

<span data-ttu-id="090b4-171">원격 컴퓨터에서 생성된 Windows PowerShell 이벤트 알림을 수신하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-171">Shows how to shows how to receive notifications of Windows PowerShell events that are generated on remote computers.</span></span>
<span data-ttu-id="090b4-172">[Runspace](/dotnet/api/system.management.automation.runspaces.runspace) 클래스를 통해 노출되는 PSEventReceived 이벤트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-172">It uses the PSEventReceived event exposed through the [Runspace](/dotnet/api/system.management.automation.runspaces.runspace) class.</span></span>

## <a name="hosting-application-samples"></a><span data-ttu-id="090b4-173">호스팅 응용 프로그램 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-173">Hosting application samples</span></span>

### <a name="runspace01"></a><span data-ttu-id="090b4-174">Runspace01</span><span class="sxs-lookup"><span data-stu-id="090b4-174">Runspace01</span></span>

<span data-ttu-id="090b4-175">[PowerShell](/dotnet/api/system.management.automation.powershell) 클래스를 사용하여 [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet을 동기적으로 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-175">Shows how to use the [PowerShell](/dotnet/api/system.management.automation.powershell) class to run the [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet synchronously.</span></span>
<span data-ttu-id="090b4-176">[Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet은 로컬 컴퓨터에서 실행 중인 각 프로세스에 대해 [Process](https://technet.microsoft.com/library/system.diagnostics.process.aspx) 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-176">The [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet returns [Process](https://technet.microsoft.com/library/system.diagnostics.process.aspx) objects for each process running on the local computer.</span></span>

### <a name="runspace02"></a><span data-ttu-id="090b4-177">Runspace02</span><span class="sxs-lookup"><span data-stu-id="090b4-177">Runspace02</span></span>

<span data-ttu-id="090b4-178">[PowerShell](/dotnet/api/system.management.automation.powershell) 클래스를 사용하여 [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) 및 [Sort-Object](/powershell/module/Microsoft.PowerShell.Utility/Sort-Object) cmdlet을 동기적으로 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-178">Shows how to use the [PowerShell](/dotnet/api/system.management.automation.powershell) class to run the [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) and [Sort-Object](/powershell/module/Microsoft.PowerShell.Utility/Sort-Object) cmdlets synchronously.</span></span>
<span data-ttu-id="090b4-179">[Get-process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet은 로컬 컴퓨터에서 실행 중인 각 프로세스에 대해 [Process](https://technet.microsoft.com/library/system.diagnostics.process.aspx) 개체를 반환하고, `Sort-Object`는 해당 [Id](https://technet.microsoft.com/library/system.diagnostics.process.id.aspx) 속성을 기준으로 개체를 정렬합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-179">The [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet returns [Process](https://technet.microsoft.com/library/system.diagnostics.process.aspx) objects for each process running on the local computer, and the `Sort-Object` sorts the objects based on their [Id](https://technet.microsoft.com/library/system.diagnostics.process.id.aspx) property.</span></span>
<span data-ttu-id="090b4-180">이러한 명령의 결과는 [DataGridView](https://technet.microsoft.com/library/system.windows.forms.datagridview.aspx) 컨트롤을 사용하여 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-180">The results of these commands is displayed by using a [DataGridView](https://technet.microsoft.com/library/system.windows.forms.datagridview.aspx) control.</span></span>

### <a name="runspace03"></a><span data-ttu-id="090b4-181">Runspace03</span><span class="sxs-lookup"><span data-stu-id="090b4-181">Runspace03</span></span>

<span data-ttu-id="090b4-182">[PowerShell](/dotnet/api/system.management.automation.powershell) 클래스를 사용하여 동기적으로 스크립트를 실행하는 방법과 종료되지 않는 오류를 처리하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-182">Shows how to use the [PowerShell](/dotnet/api/system.management.automation.powershell) class to run a script synchronously, and how to handle non-terminating errors.</span></span>
<span data-ttu-id="090b4-183">스크립트는 프로세스 이름 목록을 받은 다음 해당 프로세스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-183">The script receives a list of process names and then retrieves those processes.</span></span>
<span data-ttu-id="090b4-184">스크립트를 실행할 때 생성된 종료되지 않는 오류를 포함하여 스크립트의 결과가 콘솔 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-184">The results of the script, including any non-terminating errors that were generated when running the script, are displayed in a console window.</span></span>

### <a name="runspace04"></a><span data-ttu-id="090b4-185">Runspace04</span><span class="sxs-lookup"><span data-stu-id="090b4-185">Runspace04</span></span>

<span data-ttu-id="090b4-186">[PowerShell](/dotnet/api/system.management.automation.powershell) 클래스를 사용하여 명령을 실행하는 방법과 명령을 실행할 때 발생한 종료 오류를 잡는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-186">Shows how to use the [PowerShell](/dotnet/api/system.management.automation.powershell) class to run commands, and how to catch terminating errors that are thrown when running the commands.</span></span>
<span data-ttu-id="090b4-187">두 개의 명령이 실행되는데, 마지막 명령은 유효하지 않은 매개 변수 인수를 전달받습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-187">Two commands are run, and the last command is passed a parameter argument that is not valid.</span></span>
<span data-ttu-id="090b4-188">따라서 개체가 반환되지 않고 종료 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-188">As a result, no objects are returned and a terminating error is thrown.</span></span>

### <a name="runspace05"></a><span data-ttu-id="090b4-189">Runspace05</span><span class="sxs-lookup"><span data-stu-id="090b4-189">Runspace05</span></span>

<span data-ttu-id="090b4-190">runspace를 열 때 스냅인의 cmdlet을 사용할 수 있도록 [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) 개체에 스냅인을 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-190">Shows how to add a snap-in to an [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) object so that the cmdlet of the snap-in is available when the runspace is opened.</span></span>
<span data-ttu-id="090b4-191">이 스냅인은 [PowerShell](/dotnet/api/system.management.automation.powershell) 개체를 사용하여 동기적으로 실행되는 Get-Proc cmdlet([GetProcessSample01 샘플](https://technet.microsoft.com/library/ff602028.aspx)에서 정의)을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-191">The snap-in provides a Get-Proc cmdlet (defined by the [GetProcessSample01 Sample](https://technet.microsoft.com/library/ff602028.aspx)) that is run synchronously by using a [PowerShell](/dotnet/api/system.management.automation.powershell) object.</span></span>

### <a name="runspace06"></a><span data-ttu-id="090b4-192">Runspace06</span><span class="sxs-lookup"><span data-stu-id="090b4-192">Runspace06</span></span>

<span data-ttu-id="090b4-193">runspace를 열 때 모듈이 로드되도록 [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) 개체에 모듈을 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-193">Shows how to add a module to an [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) object so that the module is loaded when the runspace is opened.</span></span>
<span data-ttu-id="090b4-194">이 모듈은 [PowerShell](/dotnet/api/system.management.automation.powershell) 개체를 사용하여 동기적으로 실행되는 Get-Proc cmdlet([GetProcessSample02 샘플](https://technet.microsoft.com/library/ff602027.aspx)에서 정의)을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-194">The module provides a Get-Proc cmdlet (defined by the [GetProcessSample02 Sample](https://technet.microsoft.com/library/ff602027.aspx)) that is run synchronously by using a [PowerShell](/dotnet/api/system.management.automation.powershell) object.</span></span>

### <a name="runspace07"></a><span data-ttu-id="090b4-195">Runspace07</span><span class="sxs-lookup"><span data-stu-id="090b4-195">Runspace07</span></span>

<span data-ttu-id="090b4-196">runspace를 만들고 해당 runspace를 사용하여 [PowerShell](/dotnet/api/system.management.automation.powershell) 개체를 통해 두 개의 cmdlet을 동기적으로 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-196">Shows how to create a runspace, and then use that runspace to run two cmdlets synchronously by using a [PowerShell](/dotnet/api/system.management.automation.powershell) object.</span></span>

### <a name="runspace08"></a><span data-ttu-id="090b4-197">Runspace08</span><span class="sxs-lookup"><span data-stu-id="090b4-197">Runspace08</span></span>

<span data-ttu-id="090b4-198">[PowerShell](/dotnet/api/system.management.automation.powershell) 개체의 파이프라인에 명령 및 인수를 추가하는 방법과 동기적으로 명령을 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-198">Shows how to add commands and arguments to the pipeline of a [PowerShell](/dotnet/api/system.management.automation.powershell) object and how to run the commands synchronously.</span></span>

### <a name="runspace09"></a><span data-ttu-id="090b4-199">Runspace09</span><span class="sxs-lookup"><span data-stu-id="090b4-199">Runspace09</span></span>

<span data-ttu-id="090b4-200">[PowerShell](/dotnet/api/system.management.automation.powershell) 개체의 파이프라인에 스크립트를 추가하는 방법과 비동기적으로 스크립트를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-200">Shows how to add a script to the pipeline of a [PowerShell](/dotnet/api/system.management.automation.powershell) object and how to run the script asynchronously.</span></span>
<span data-ttu-id="090b4-201">이벤트는 스크립트의 출력을 처리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-201">Events are used to handle the output of the script.</span></span>

### <a name="runspace10"></a><span data-ttu-id="090b4-202">Runspace10</span><span class="sxs-lookup"><span data-stu-id="090b4-202">Runspace10</span></span>

<span data-ttu-id="090b4-203">기본 초기 세션 상태를 만드는 방법, [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate)에 cmdlet을 추가하는 방법, 초기 세션 상태를 사용하는 runspace를 만드는 방법 및 [PowerShell](/dotnet/api/system.management.automation.powershell) 개체를 사용하여 명령을 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-203">Shows how to create a default initial session state, how to add a cmdlet to the [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate), how to create a runspace that uses the initial session state, and how to run the command by using a [PowerShell](/dotnet/api/system.management.automation.powershell) object.</span></span>

### <a name="runspace11"></a><span data-ttu-id="090b4-204">Runspace11</span><span class="sxs-lookup"><span data-stu-id="090b4-204">Runspace11</span></span>

<span data-ttu-id="090b4-205">[ProxyCommand](/dotnet/api/system.management.automation.proxycommand) 클래스를 사용하여 기존 cmdlet을 호출하지만 사용 가능한 매개 변수 집합을 제한하는 프록시 명령을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-205">Shows how to use the [ProxyCommand](/dotnet/api/system.management.automation.proxycommand) class to create a proxy command that calls an existing cmdlet, but restricts the set of available parameters.</span></span>
<span data-ttu-id="090b4-206">프록시 명령은 제한된 runspace를 만드는 데 사용되는 초기 세션 상태에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-206">The proxy command is then added to an initial session state that is used to create a constrained runspace.</span></span>
<span data-ttu-id="090b4-207">따라서 사용자가 프록시 명령을 통해서만 cmdlet의 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-207">This means that the user can access the functionality of the cmdlet only through the proxy command.</span></span>

### <a name="powershell01"></a><span data-ttu-id="090b4-208">PowerShell01</span><span class="sxs-lookup"><span data-stu-id="090b4-208">PowerShell01</span></span>

<span data-ttu-id="090b4-209">[InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) 개체를 사용하여 제한된 runspace를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-209">Shows how to create a constrained runspace using an [InitialSessionState](/dotnet/api/system.management.automation.runspaces.initialsessionstate) object.</span></span>

### <a name="powershell02"></a><span data-ttu-id="090b4-210">PowerShell02</span><span class="sxs-lookup"><span data-stu-id="090b4-210">PowerShell02</span></span>

<span data-ttu-id="090b4-211">runspace 풀을 사용하여 여러 명령을 동시에 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-211">Shows how to use a runspace pool to run multiple commands concurrently.</span></span>

## <a name="host-samples"></a><span data-ttu-id="090b4-212">호스트 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-212">Host samples</span></span>

### <a name="host01"></a><span data-ttu-id="090b4-213">Host01</span><span class="sxs-lookup"><span data-stu-id="090b4-213">Host01</span></span>

<span data-ttu-id="090b4-214">사용자 지정 호스트를 사용하는 호스트 응용 프로그램을 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-214">Shows how to implement a host application that uses a custom host.</span></span>
<span data-ttu-id="090b4-215">이 샘플에서는 사용자 지정 호스트를 사용하는 runspace를 만든 다음 [PowerShell](/dotnet/api/system.management.automation.powershell) API를 사용하여 "종료"를 호출하는 스크립트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-215">In this sample a runspace is created that uses the custom host, and then the [PowerShell](/dotnet/api/system.management.automation.powershell) API is used to run a script that calls "exit".</span></span>
<span data-ttu-id="090b4-216">호스트 응용 프로그램은 스크립트의 출력을 살펴보고 결과를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-216">The host application then looks at the output of the script and prints out the results.</span></span>

### <a name="host02"></a><span data-ttu-id="090b4-217">Host02</span><span class="sxs-lookup"><span data-stu-id="090b4-217">Host02</span></span>

<span data-ttu-id="090b4-218">사용자 지정 호스트 구현과 함께 Windows PowerShell 런타임을 사용하는 호스트 응용 프로그램을 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-218">Shows how to write a host application that uses the Windows PowerShell runtime along with a custom host implementation.</span></span>
<span data-ttu-id="090b4-219">호스트 응용 프로그램은 호스트 문화권을 독일어로 설정하고, [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet을 실행한 다음 pwrsh.exe를 사용하여 보이는 대로 결과를 표시하고 현재 날짜와 시간을 독일어로 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-219">The host application sets the host culture to German, runs the [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet and displays the results as you would see them by using pwrsh.exe, and then prints out the current data and time in German.</span></span>

### <a name="host03"></a><span data-ttu-id="090b4-220">Host03</span><span class="sxs-lookup"><span data-stu-id="090b4-220">Host03</span></span>

<span data-ttu-id="090b4-221">명령줄에서 명령을 읽고 명령을 실행한 후 콘솔에 결과를 표시하는 대화형 콘솔 기반 호스트 응용 프로그램을 구축하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-221">Shows how to build an interactive console-based host application that reads commands from the command line, executes the commands, and then displays the results to the console.</span></span>

### <a name="host04"></a><span data-ttu-id="090b4-222">Host04</span><span class="sxs-lookup"><span data-stu-id="090b4-222">Host04</span></span>

<span data-ttu-id="090b4-223">명령줄에서 명령을 읽고 명령을 실행한 후 콘솔에 결과를 표시하는 대화형 콘솔 기반 호스트 응용 프로그램을 구축하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-223">Shows how to build an interactive console-based host application that reads commands from the command line, executes the commands, and then displays the results to the console.</span></span>
<span data-ttu-id="090b4-224">이 호스트 응용 프로그램은 사용자가 여러 선택 항목을 지정할 수 있는 프롬프트 표시도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-224">This host application also supports displaying prompts that allow the user to specify multiple choices.</span></span>

### <a name="host05"></a><span data-ttu-id="090b4-225">Host05</span><span class="sxs-lookup"><span data-stu-id="090b4-225">Host05</span></span>

<span data-ttu-id="090b4-226">명령줄에서 명령을 읽고 명령을 실행한 후 콘솔에 결과를 표시하는 대화형 콘솔 기반 호스트 응용 프로그램을 구축하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-226">Shows how to build an interactive console-based host application that reads commands from the command line, executes the commands, and then displays the results to the console.</span></span>
<span data-ttu-id="090b4-227">이 호스트 응용 프로그램은 [Enter-PsSession](/powershell/module/Microsoft.PowerShell.Core/Enter-PSSession) 및 [Exit-PsSession](/powershell/module/Microsoft.PowerShell.Core/Exit-PSSession) cmdlet을 사용한 원격 컴퓨터 호출도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-227">This host application also supports calls to remote computers by using the [Enter-PsSession](/powershell/module/Microsoft.PowerShell.Core/Enter-PSSession) and [Exit-PsSession](/powershell/module/Microsoft.PowerShell.Core/Exit-PSSession) cmdlets.</span></span>

### <a name="host06"></a><span data-ttu-id="090b4-228">Host06</span><span class="sxs-lookup"><span data-stu-id="090b4-228">Host06</span></span>

<span data-ttu-id="090b4-229">명령줄에서 명령을 읽고 명령을 실행한 후 콘솔에 결과를 표시하는 대화형 콘솔 기반 호스트 응용 프로그램을 구축하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-229">Shows how to build an interactive console-based host application that reads commands from the command line, executes the commands, and then displays the results to the console.</span></span>
<span data-ttu-id="090b4-230">또한 이 샘플에서는 토크나이저 API를 사용하여 사용자가 입력하는 텍스트의 색을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-230">In addition, this sample uses the Tokenizer APIs to specify the color of the text that is entered by the user.</span></span>

## <a name="provider-samples"></a><span data-ttu-id="090b4-231">공급자 샘플</span><span class="sxs-lookup"><span data-stu-id="090b4-231">Provider samples</span></span>

### <a name="accessdbprovidersample01"></a><span data-ttu-id="090b4-232">AccessDBProviderSample01</span><span class="sxs-lookup"><span data-stu-id="090b4-232">AccessDBProviderSample01</span></span>

<span data-ttu-id="090b4-233">[CmdletProvider](/dotnet/api/system.management.automation.provider.cmdletprovider) 클래스에서 직접 파생되는 공급자 클래스를 선언하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-233">Shows how to declare a provider class that derives directly from the [CmdletProvider](/dotnet/api/system.management.automation.provider.cmdletprovider) class.</span></span>
<span data-ttu-id="090b4-234">여기서는 참조용으로만 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-234">It is included here only for completeness.</span></span>

### <a name="accessdbprovidersample02"></a><span data-ttu-id="090b4-235">AccessDBProviderSample02</span><span class="sxs-lookup"><span data-stu-id="090b4-235">AccessDBProviderSample02</span></span>

<span data-ttu-id="090b4-236">`New-PSDrive` 및 `Remove-PSDrive` cmdlet 호출을 지원하기 위해 [NewDrive](/dotnet/api/system.management.automation.provider.drivecmdletprovider.newdrive) 및 [RemoveDrive](/dotnet/api/system.management.automation.provider.drivecmdletprovider.removedrive) 메서드를 덮어쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-236">Shows how to overwrite the [NewDrive](/dotnet/api/system.management.automation.provider.drivecmdletprovider.newdrive) and [RemoveDrive](/dotnet/api/system.management.automation.provider.drivecmdletprovider.removedrive) methods to support calls to the `New-PSDrive` and `Remove-PSDrive` cmdlets.</span></span>
<span data-ttu-id="090b4-237">이 샘플의 공급자 클래스는 [DriveCmdletProvider](/dotnet/api/system.management.automation.provider.drivecmdletprovider) 클래스에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-237">The provider class in this sample derives from the [DriveCmdletProvider](/dotnet/api/system.management.automation.provider.drivecmdletprovider) class.</span></span>

### <a name="accessdbprovidersample03"></a><span data-ttu-id="090b4-238">AccessDBProviderSample03</span><span class="sxs-lookup"><span data-stu-id="090b4-238">AccessDBProviderSample03</span></span>

<span data-ttu-id="090b4-239">`Get-Item` 및 `Set-Item` cmdlet 호출을 지원하기 위해 [GetItem](/dotnet/api/system.management.automation.provider.itemcmdletprovider.getitem) 및 [SetItem](/dotnet/api/system.management.automation.provider.itemcmdletprovider.setitem) 메서드를 덮어쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-239">Shows how to overwrite the [GetItem](/dotnet/api/system.management.automation.provider.itemcmdletprovider.getitem) and [SetItem](/dotnet/api/system.management.automation.provider.itemcmdletprovider.setitem) methods to support calls to the `Get-Item` and `Set-Item` cmdlets.</span></span>
<span data-ttu-id="090b4-240">이 샘플의 공급자 클래스는 [ItemCmdletProvider](/dotnet/api/system.management.automation.provider.itemcmdletprovider) 클래스에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-240">The provider class in this sample derives from the [ItemCmdletProvider](/dotnet/api/system.management.automation.provider.itemcmdletprovider) class.</span></span>

### <a name="accessdbprovidersample04"></a><span data-ttu-id="090b4-241">AccessDBProviderSample04</span><span class="sxs-lookup"><span data-stu-id="090b4-241">AccessDBProviderSample04</span></span>

<span data-ttu-id="090b4-242">`Copy-Item`, `Get-ChildItem`, `New-Item` 및 `Remove-Item` cmdlet 호출을 지원하기 위해 컨테이너 메서드를 덮어쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-242">Shows how to overwrite container methods to support calls to the `Copy-Item`, `Get-ChildItem`, `New-Item`, and `Remove-Item` cmdlets.</span></span>
<span data-ttu-id="090b4-243">이러한 메서드는 데이터 저장소에 컨테이너 항목이 포함될 때 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-243">These methods should be implemented when the data store contains items that are containers.</span></span>
<span data-ttu-id="090b4-244">컨테이너는 공통 부모 항목 아래에 있는 자식 항목 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-244">A container is a group of child items under a common parent item.</span></span>
<span data-ttu-id="090b4-245">이 샘플의 공급자 클래스는 [ItemCmdletProvider](/dotnet/api/system.management.automation.provider.itemcmdletprovider) 클래스에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-245">The provider class in this sample derives from the [ItemCmdletProvider](/dotnet/api/system.management.automation.provider.itemcmdletprovider) class.</span></span>

### <a name="accessdbprovidersample05"></a><span data-ttu-id="090b4-246">AccessDBProviderSample05</span><span class="sxs-lookup"><span data-stu-id="090b4-246">AccessDBProviderSample05</span></span>

<span data-ttu-id="090b4-247">`Move-Item` 및 `Join-Path` cmdlet 호출을 지원하기 위해 컨테이너 메서드를 덮어쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-247">Shows how to overwrite container methods to support calls to the `Move-Item` and `Join-Path` cmdlets.</span></span>
<span data-ttu-id="090b4-248">이러한 메서드는 사용자가 컨테이너 내의 항목을 이동해야 하고 데이터 저장소에 중첩된 컨테이너가 포함되는 경우에 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-248">These methods should be implemented when the user needs to move items within a container and if the data store contains nested containers.</span></span>
<span data-ttu-id="090b4-249">이 샘플의 공급자 클래스는 [NavigationCmdletProvider](/dotnet/api/system.management.automation.provider.navigationcmdletprovider) 클래스에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-249">The provider class in this sample derives from the [NavigationCmdletProvider](/dotnet/api/system.management.automation.provider.navigationcmdletprovider) class.</span></span>

### <a name="accessdbprovidersample06"></a><span data-ttu-id="090b4-250">AccessDBProviderSample06</span><span class="sxs-lookup"><span data-stu-id="090b4-250">AccessDBProviderSample06</span></span>

<span data-ttu-id="090b4-251">`Clear-Content`, `Get-Content` 및 `Set-Content` cmdlet 호출을 지원하기 위해 컨테이너 메서드를 덮어쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-251">Shows how to overwrite content methods to support calls to the `Clear-Content`, `Get-Content`, and `Set-Content` cmdlets.</span></span>
<span data-ttu-id="090b4-252">이러한 메서드는 사용자가 데이터 저장소에 있는 항목의 콘텐츠를 관리해야 하는 경우에 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-252">These methods should be implemented when the user needs to manage the content of the items in the data store.</span></span>
<span data-ttu-id="090b4-253">이 샘플의 공급자 클래스는 [NavigationCmdletProvider](/dotnet/api/system.management.automation.provider.navigationcmdletprovider) 클래스에서 파생되며, [IContentCmdletProvider](/dotnet/api/system.management.automation.provider.icontentcmdletprovider) 인터페이스를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="090b4-253">The provider class in this sample derives from the [NavigationCmdletProvider](/dotnet/api/system.management.automation.provider.navigationcmdletprovider) class, and it implements the [IContentCmdletProvider](/dotnet/api/system.management.automation.provider.icontentcmdletprovider) interface.</span></span>