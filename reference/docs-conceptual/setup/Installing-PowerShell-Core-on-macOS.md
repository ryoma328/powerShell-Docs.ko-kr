---
title: macOS에서 PowerShell Core 설치
description: macOS에서 PowerShell Core를 설치하는 방법에 대한 정보
ms.date: 08/06/2018
ms.openlocfilehash: 042c933dfa83f3ab52e315036e4f817145116d00
ms.sourcegitcommit: aa41249f153bbc6e11667ade60c878980c15abc6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45611490"
---
# <a name="installing-powershell-core-on-macos"></a><span data-ttu-id="77e76-103">macOS에서 PowerShell Core 설치</span><span class="sxs-lookup"><span data-stu-id="77e76-103">Installing PowerShell Core on macOS</span></span>

<span data-ttu-id="77e76-104">PowerShell Core는 macOS 10.12 이상을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-104">PowerShell Core supports macOS 10.12 and higher.</span></span>
<span data-ttu-id="77e76-105">모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-105">All packages are available on our GitHub [releases][] page.</span></span>
<span data-ttu-id="77e76-106">패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-106">Once the package is installed, run `pwsh` from a terminal.</span></span>

## <a name="installation-of-latest-stable-release-via-homebrew-on-macos-1012-or-higher"></a><span data-ttu-id="77e76-107">macOS 10.12 이상에서 Homebrew를 통해 안정적인 최신 릴리스 설치</span><span class="sxs-lookup"><span data-stu-id="77e76-107">Installation of latest stable release via Homebrew on macOS 10.12 or higher</span></span>

<span data-ttu-id="77e76-108">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-108">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="77e76-109">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-109">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

<span data-ttu-id="77e76-110">이제 PowerShell을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-110">Now, you can install PowerShell:</span></span>

```sh
brew cask install powershell
```

<span data-ttu-id="77e76-111">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-111">Finally, verify that your install is working properly:</span></span>

```sh
pwsh
```

<span data-ttu-id="77e76-112">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-112">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> <span data-ttu-id="77e76-113">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만, 업그레이드를 완료하기 위해 PowerShell 셸을 종료하고 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-113">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade.</span></span>
> <span data-ttu-id="77e76-114">$PSVersionTable에 표시된 값을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-114">and refresh the values shown in $PSVersionTable.</span></span>

[brew]: http://brew.sh/

## <a name="installation-of-latest-preview-release-via-homebrew-on-macos-1012-or-higher"></a><span data-ttu-id="77e76-115">macOS 10.12 이상에서 Homebrew를 통해 최신 미리 보기 릴리스 설치</span><span class="sxs-lookup"><span data-stu-id="77e76-115">Installation of latest preview release via Homebrew on macOS 10.12 or higher</span></span>

<span data-ttu-id="77e76-116">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-116">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="77e76-117">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-117">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

<span data-ttu-id="77e76-118">Homebrew를 설치했으면 PowerShell을 쉽게 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-118">Once you've installed Homebrew, installing PowerShell is easy.</span></span>
<span data-ttu-id="77e76-119">먼저, Cask 패키지의 다른 버전을 설치할 수 있는 [Cask-버전][cask-versions]을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-119">First, install [Cask-Versions][cask-versions] which lets you install alternative versions of cask packages:</span></span>

```sh
brew tap homebrew/cask-versions
```

<span data-ttu-id="77e76-120">이제 PowerShell을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-120">Now, you can install PowerShell:</span></span>

```sh
brew cask install powershell-preview
```

<span data-ttu-id="77e76-121">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-121">Finally, verify that your install is working properly:</span></span>

```sh
pwsh-preview
```

<span data-ttu-id="77e76-122">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-122">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> <span data-ttu-id="77e76-123">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만, 업그레이드를 완료하기 위해 PowerShell 셸을 종료하고 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-123">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade.</span></span>
> <span data-ttu-id="77e76-124">$PSVersionTable에 표시된 값을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-124">and refresh the values shown in $PSVersionTable.</span></span>

## <a name="installation-via-direct-download"></a><span data-ttu-id="77e76-125">직접 다운로드를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="77e76-125">Installation via Direct Download</span></span>

<span data-ttu-id="77e76-126">PKG 패키지 `powershell-6.1.0-osx-x64.pkg`를</span><span class="sxs-lookup"><span data-stu-id="77e76-126">Download the PKG package `powershell-6.1.0-osx-x64.pkg`</span></span>
<span data-ttu-id="77e76-127">[릴리스][] 페이지에서 macOS 머신으로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-127">from the [releases][] page onto your macOS machine.</span></span>

<span data-ttu-id="77e76-128">파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-128">You can double-click the file and follow the prompts, or install it from the terminal:</span></span>

```sh
sudo installer -pkg powershell-6.1.0-osx-x64.pkg -target /
```

## <a name="binary-archives"></a><span data-ttu-id="77e76-129">이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="77e76-129">Binary Archives</span></span>

<span data-ttu-id="77e76-130">고급 배포 시나리오를 사용하도록 설정하려면 macOS 플랫폼에 대해 PowerShell 이진 `tar.gz` 보관이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-130">PowerShell binary `tar.gz` archives are provided for the macOS platform to enable advanced deployment scenarios.</span></span>

### <a name="installing-binary-archives-on-macos"></a><span data-ttu-id="77e76-131">macOS에서 이진 보관 설치</span><span class="sxs-lookup"><span data-stu-id="77e76-131">Installing binary archives on macOS</span></span>

```sh
# Download the powershell '.tar.gz' archive
curl -L -o /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v6.1.0/powershell-6.1.0-osx-x64.tar.gz

# Create the target folder where powershell will be placed
sudo mkdir -p /usr/local/microsoft/powershell/6.1.0

# Expand powershell to the target folder
sudo tar zxf /tmp/powershell.tar.gz -C /usr/local/microsoft/powershell/6.1.0

# Set execute permissions
sudo chmod +x /usr/local/microsoft/powershell/6.1.0/pwsh

# Create the symbolic link that points to pwsh
sudo ln -s /usr/local/microsoft/powershell/6.1.0/pwsh /usr/local/bin/pwsh
```

## <a name="uninstalling-powershell-core"></a><span data-ttu-id="77e76-132">PowerShell Core 제거</span><span class="sxs-lookup"><span data-stu-id="77e76-132">Uninstalling PowerShell Core</span></span>

<span data-ttu-id="77e76-133">Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-133">If you installed PowerShell with Homebrew, uninstallation is easy:</span></span>

```sh
brew cask uninstall powershell
```

<span data-ttu-id="77e76-134">직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-134">If you installed PowerShell via direct download, PowerShell must be removed manually:</span></span>

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

<span data-ttu-id="77e76-135">추가 PowerShell 경로를 제거하려면 이 문서의 [경로](#paths) 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-135">To remove the additional PowerShell paths, please see the [paths](#paths) section in this document and remove the desired the paths using `sudo rm`.</span></span>

> [!NOTE]
> <span data-ttu-id="77e76-136">Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-136">This is not necessary if you installed with Homebrew.</span></span>

## <a name="paths"></a><span data-ttu-id="77e76-137">경로</span><span class="sxs-lookup"><span data-stu-id="77e76-137">Paths</span></span>

* <span data-ttu-id="77e76-138">`$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`입니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-138">`$PSHOME` is `/usr/local/microsoft/powershell/6.1.0/`</span></span>
* <span data-ttu-id="77e76-139">사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-139">User profiles will be read from `~/.config/powershell/profile.ps1`</span></span>
* <span data-ttu-id="77e76-140">기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-140">Default profiles will be read from `$PSHOME/profile.ps1`</span></span>
* <span data-ttu-id="77e76-141">사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-141">User modules will be read from `~/.local/share/powershell/Modules`</span></span>
* <span data-ttu-id="77e76-142">공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-142">Shared modules will be read from `/usr/local/share/powershell/Modules`</span></span>
* <span data-ttu-id="77e76-143">기본 모듈은 `$PSHOME/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-143">Default modules will be read from `$PSHOME/Modules`</span></span>
* <span data-ttu-id="77e76-144">PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-144">PSReadline history will be recorded to `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`</span></span>

<span data-ttu-id="77e76-145">프로필은 PowerShell의 호스트별 구성을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-145">The profiles respect PowerShell's per-host configuration.</span></span>
<span data-ttu-id="77e76-146">따라서 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-146">So the default host-specific profiles exists at `Microsoft.PowerShell_profile.ps1` in the same locations.</span></span>

<span data-ttu-id="77e76-147">PowerShell은 macOS의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-147">PowerShell respects the [XDG Base Directory Specification][xdg-bds] on macOS.</span></span>

<span data-ttu-id="77e76-148">macOS는 BSD에서 파생된 것이므로 `/opt` 대신 `/usr/local`이 접두사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-148">Because macOS is a derivation of BSD, the prefix `/usr/local` is used instead of `/opt`.</span></span>
<span data-ttu-id="77e76-149">따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`이며 symlink는 `/usr/local/bin/pwsh`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e76-149">Thus, `$PSHOME` is `/usr/local/microsoft/powershell/6.1.0/`, and the symlink is placed at `/usr/local/bin/pwsh`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77e76-150">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="77e76-150">Additional Resources</span></span>

* <span data-ttu-id="77e76-151">[Homebrew 웹][brew]</span><span class="sxs-lookup"><span data-stu-id="77e76-151">[Homebrew Web][brew]</span></span>
* <span data-ttu-id="77e76-152">[Homebrew Github 리포지토리][GitHub]</span><span class="sxs-lookup"><span data-stu-id="77e76-152">[Homebrew Github Repository][GitHub]</span></span>
* <span data-ttu-id="77e76-153">[Homebrew-Cask][cask]</span><span class="sxs-lookup"><span data-stu-id="77e76-153">[Homebrew-Cask][cask]</span></span>

[brew]: http://brew.sh/
[Cask]: https://github.com/Homebrew/homebrew-cask
[cask-versions]: https://github.com/Homebrew/homebrew-cask-versions
[GitHub]: https://github.com/Homebrew
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[releases]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
