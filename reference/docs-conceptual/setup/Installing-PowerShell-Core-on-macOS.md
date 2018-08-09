---
title: macOS에서 PowerShell Core 설치
description: macOS에서 PowerShell Core를 설치하는 방법에 대한 정보
ms.date: 08/06/2018
ms.openlocfilehash: ff1814d95b3ca3fa8497069dff249fd2ad5576ef
ms.sourcegitcommit: 01ac77cd0b00e4e5e964504563a9212e8002e5e0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2018
ms.locfileid: "39587468"
---
# <a name="installing-powershell-core-on-macos"></a><span data-ttu-id="b33d1-103">macOS에서 PowerShell Core 설치</span><span class="sxs-lookup"><span data-stu-id="b33d1-103">Installing PowerShell Core on macOS</span></span>

<span data-ttu-id="b33d1-104">PowerShell Core는 macOS 10.12 이상을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-104">PowerShell Core supports macOS 10.12 and higher.</span></span>
<span data-ttu-id="b33d1-105">모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-105">All packages are available on our GitHub [releases][] page.</span></span>
<span data-ttu-id="b33d1-106">패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-106">Once the package is installed, run `pwsh` from a terminal.</span></span>

### <a name="installation-via-homebrew-on-macos-1012"></a><span data-ttu-id="b33d1-107">macOS 10.12 이상에서 Homebrew를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="b33d1-107">Installation via Homebrew on macOS 10.12+</span></span>

<span data-ttu-id="b33d1-108">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-108">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="b33d1-109">터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-109">From a terminal window, type `brew` to run Homebrew.</span></span>  <span data-ttu-id="b33d1-110">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-110">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

> [!NOTE]
> <span data-ttu-id="b33d1-111">이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-111">If you installed Homebrew in the past, it's always a good idea to run 'brew update-reset' && 'brew update'.</span></span>
```sh
brew update-reset
brew update
```

> <span data-ttu-id="b33d1-112">Homebrew의 이전 버전에서는 ‘caskroom/cask’를 사용했으나, 더 이상 사용되지 않고 ‘homebrew/cask’로 마이그레이션되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-112">Older versions of Homebrew used the tap 'caskroom/cask', which has been deprecated, and migrated into 'homebrew/cask'.</span></span>  <span data-ttu-id="b33d1-113">자세한 내용은 [Homebrew-cask][cask]를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b33d1-113">More information can be found at [Homebrew-cask][cask].</span></span> <span data-ttu-id="b33d1-114">‘brew tap’ 명령을 사용하여 현재 탭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-114">Use the 'brew tap' command to list your current taps.</span></span>  <span data-ttu-id="b33d1-115">‘caskroom/cask’가 표시되면 ‘brew update’를 사용하여 Homebrew가 탭을 마이그레이션하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-115">If you see 'caskroom/cask' you can use 'brew update' to have Homebrew migrate the taps.</span></span>

```sh
brew tap
brew update
```

<span data-ttu-id="b33d1-116">Homebrew를 설치/업데이트한 후 PowerShell을 쉽게 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-116">Once you've installed/updated Homebrew, installing PowerShell is easy.</span></span>

<span data-ttu-id="b33d1-117">PowerShell을 설치하려면</span><span class="sxs-lookup"><span data-stu-id="b33d1-117">To install PowerShell:</span></span>

```sh
brew cask install powershell
```

<span data-ttu-id="b33d1-118">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-118">Finally, verify that your install is working properly:</span></span>

```sh
pwsh
```

<span data-ttu-id="b33d1-119">PowerShell을 종료하고 bash로 돌아가려면 ‘exit’ 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-119">To exit PowerShell, and return to bash, use the 'exit' command.</span></span>
```sh
exit
```

<span data-ttu-id="b33d1-120">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-120">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> <span data-ttu-id="b33d1-121">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-121">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade and refresh the values shown in $PSVersionTable.</span></span>

### <a name="installing-preview-via-homebrew-on-macos-1012"></a><span data-ttu-id="b33d1-122">macOS 10.12 이상에서 Homebrew를 통해 미리 보기 설치</span><span class="sxs-lookup"><span data-stu-id="b33d1-122">Installing Preview via Homebrew on macOS 10.12+</span></span>

<span data-ttu-id="b33d1-123">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-123">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="b33d1-124">터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-124">From a terminal window, type `brew` to run Homebrew.</span></span>  <span data-ttu-id="b33d1-125">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-125">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

> [!NOTE]
> <span data-ttu-id="b33d1-126">이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-126">If you installed Homebrew in the past, it's always a good idea to run 'brew update-reset' && 'brew update'.</span></span>
```sh
brew update-reset
brew update
```

<span data-ttu-id="b33d1-127">그런 다음, 미리 보기 패키지를 가져오려면 `versions` casks 리포지토리를 탭해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-127">Then, you must tap the `versions` casks repository to get the preview package:</span></span>

```sh
brew tap homebrew/cask-versions
```

<span data-ttu-id="b33d1-128">PowerShell 미리 보기를 설치하려면:</span><span class="sxs-lookup"><span data-stu-id="b33d1-128">To install PowerShell Preview:</span></span>

```sh
brew cask install powershell-preview
```

<span data-ttu-id="b33d1-129">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-129">Finally, verify that your install is working properly:</span></span>

```sh
pwsh-preview
```

<span data-ttu-id="b33d1-130">PowerShell의 새 버전이 릴리스되면 Homebrew의 수식을 업데이트하고 PowerShell 미리 보기를 업그레이드하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-130">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell Preview:</span></span>

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> <span data-ttu-id="b33d1-131">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-131">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade and refresh the values shown in $PSVersionTable.</span></span>

### <a name="installation-via-direct-download"></a><span data-ttu-id="b33d1-132">직접 다운로드를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="b33d1-132">Installation via Direct Download</span></span>

<span data-ttu-id="b33d1-133">[릴리스][] 페이지의 PKG 패키지 `powershell-6.0.2-osx.10.12-x64.pkg`를 macOS 컴퓨터로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-133">Download the PKG package `powershell-6.0.2-osx.10.12-x64.pkg` from the [releases][] page onto your macOS machine.</span></span>

<span data-ttu-id="b33d1-134">파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-134">You can double-click the file and follow the prompts, or install it from the terminal:</span></span>

```sh
sudo installer -pkg powershell-6.0.2-osx.10.12-x64.pkg -target /
```

## <a name="binary-archives"></a><span data-ttu-id="b33d1-135">이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="b33d1-135">Binary Archives</span></span>

<span data-ttu-id="b33d1-136">고급 배포 시나리오를 지원하기 위해 macOS 및 Linux 플랫폼에 PowerShell 이진 `tar.gz` 아카이브가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-136">PowerShell binary `tar.gz` archives are provided for macOS and Linux platforms to enable advanced deployment scenarios.</span></span>

### <a name="installing-binary-archives-on-macos"></a><span data-ttu-id="b33d1-137">macOS에서 이진 보관 설치</span><span class="sxs-lookup"><span data-stu-id="b33d1-137">Installing binary archives on macOS</span></span>

```sh
# Download the powershell '.tar.gz' archive
curl -L -o /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-osx-x64.tar.gz

# Create the target folder where powershell will be placed
sudo mkdir -p /usr/local/microsoft/powershell/6.0.2

# Expand powershell to the target folder
sudo tar zxf /tmp/powershell.tar.gz -C /usr/local/microsoft/powershell/6.0.2

# Set execute permissions
sudo chmod +x /usr/local/microsoft/powershell/6.0.2/pwsh

# Create the symbolic link that points to pwsh
sudo ln -s /usr/local/microsoft/powershell/6.0.2/pwsh /usr/local/bin/pwsh
```

## <a name="uninstalling-powershell-core"></a><span data-ttu-id="b33d1-138">PowerShell Core 제거</span><span class="sxs-lookup"><span data-stu-id="b33d1-138">Uninstalling PowerShell Core</span></span>

<span data-ttu-id="b33d1-139">Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-139">If you installed PowerShell with Homebrew, uninstallation is easy:</span></span>

```sh
brew cask uninstall powershell
```

<span data-ttu-id="b33d1-140">직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-140">If you installed PowerShell via direct download, PowerShell must be removed manually:</span></span>

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

<span data-ttu-id="b33d1-141">추가 PowerShell 경로를 제거하려면 이 문서의 [경로][] 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-141">To remove the additional PowerShell paths, please see the [paths][] section in this document and remove the desired the paths using `sudo rm`.</span></span>

> [!NOTE]
> <span data-ttu-id="b33d1-142">Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-142">This is not necessary if you installed with Homebrew.</span></span>

[경로]:#paths
[paths]:#paths

## <a name="paths"></a><span data-ttu-id="b33d1-144">경로</span><span class="sxs-lookup"><span data-stu-id="b33d1-144">Paths</span></span>

* <span data-ttu-id="b33d1-145">`$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`입니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-145">`$PSHOME` is `/usr/local/microsoft/powershell/6.0.2/`</span></span>
* <span data-ttu-id="b33d1-146">사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-146">User profiles will be read from `~/.config/powershell/profile.ps1`</span></span>
* <span data-ttu-id="b33d1-147">기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-147">Default profiles will be read from `$PSHOME/profile.ps1`</span></span>
* <span data-ttu-id="b33d1-148">사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-148">User modules will be read from `~/.local/share/powershell/Modules`</span></span>
* <span data-ttu-id="b33d1-149">공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-149">Shared modules will be read from `/usr/local/share/powershell/Modules`</span></span>
* <span data-ttu-id="b33d1-150">기본 모듈은 `$PSHOME/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-150">Default modules will be read from `$PSHOME/Modules`</span></span>
* <span data-ttu-id="b33d1-151">PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-151">PSReadline history will be recorded to `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`</span></span>

<span data-ttu-id="b33d1-152">프로필은 PowerShell의 호스트별 구성을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-152">The profiles respect PowerShell's per-host configuration.</span></span>
<span data-ttu-id="b33d1-153">따라서 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-153">So the default host-specific profiles exists at `Microsoft.PowerShell_profile.ps1` in the same locations.</span></span>

<span data-ttu-id="b33d1-154">PowerShell은 macOS의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-154">PowerShell respects the [XDG Base Directory Specification][xdg-bds] on macOS.</span></span>

<span data-ttu-id="b33d1-155">macOS는 BSD에서 파생된 것이므로 `/opt` 대신 `/usr/local`이 접두사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-155">Because macOS is a derivation of BSD, the prefix `/usr/local` is used instead of `/opt`.</span></span>
<span data-ttu-id="b33d1-156">따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`이며 symlink는 `/usr/local/bin/pwsh`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b33d1-156">Thus, `$PSHOME` is `/usr/local/microsoft/powershell/6.0.2/`, and the symlink is placed at `/usr/local/bin/pwsh`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b33d1-157">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="b33d1-157">Additional Resources</span></span>

* <span data-ttu-id="b33d1-158">[Homebrew 웹][brew]</span><span class="sxs-lookup"><span data-stu-id="b33d1-158">[Homebrew Web][brew]</span></span>
* <span data-ttu-id="b33d1-159">[Homebrew Github 리포지토리][GitHub]</span><span class="sxs-lookup"><span data-stu-id="b33d1-159">[Homebrew Github Repository][GitHub]</span></span>
* <span data-ttu-id="b33d1-160">[Homebrew-Cask][cask]</span><span class="sxs-lookup"><span data-stu-id="b33d1-160">[Homebrew-Cask][cask]</span></span>


[brew]: http://brew.sh/
[GitHub]: https://github.com/Homebrew
[Cask]: https://github.com/Homebrew/homebrew-cask
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[releases]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
