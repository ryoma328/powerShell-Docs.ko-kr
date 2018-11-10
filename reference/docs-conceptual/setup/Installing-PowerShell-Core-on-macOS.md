---
title: macOS에서 PowerShell Core 설치
description: macOS에서 PowerShell Core를 설치하는 방법에 대한 정보
ms.date: 11/02/2018
ms.openlocfilehash: 162e841bf71d708e9db84ea1bb2dbef13924783b
ms.sourcegitcommit: f4247d3f91d06ec392c4cd66921ce7d0456a2bd9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2018
ms.locfileid: "50998506"
---
# <a name="installing-powershell-core-on-macos"></a><span data-ttu-id="4a047-103">macOS에서 PowerShell Core 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-103">Installing PowerShell Core on macOS</span></span>

<span data-ttu-id="4a047-104">PowerShell Core는 macOS 10.12 이상을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-104">PowerShell Core supports macOS 10.12 and higher.</span></span>
<span data-ttu-id="4a047-105">모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-105">All packages are available on our GitHub [releases][] page.</span></span>
<span data-ttu-id="4a047-106">패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-106">Once the package is installed, run `pwsh` from a terminal.</span></span>

## <a name="about-brew"></a><span data-ttu-id="4a047-107">Brew 정보</span><span class="sxs-lookup"><span data-stu-id="4a047-107">About Brew</span></span>

<span data-ttu-id="4a047-108">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-108">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="4a047-109">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-109">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

## <a name="installation-of-latest-stable-release-via-homebrew-on-macos-1012-or-higher"></a><span data-ttu-id="4a047-110">macOS 10.12 이상에서 Homebrew를 통해 안정적인 최신 릴리스 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-110">Installation of latest stable release via Homebrew on macOS 10.12 or higher</span></span>

<span data-ttu-id="4a047-111">Brew에 대한 자세한 내용은 [Brew정보](#about-brew)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a047-111">See [About Brew](#about-brew) for information about Brew.</span></span>

<span data-ttu-id="4a047-112">이제 PowerShell을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-112">Now, you can install PowerShell:</span></span>

```sh
brew cask install powershell
```

<span data-ttu-id="4a047-113">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-113">Finally, verify that your install is working properly:</span></span>

```sh
pwsh
```

<span data-ttu-id="4a047-114">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-114">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> <span data-ttu-id="4a047-115">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-115">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade and refresh the values shown in $PSVersionTable.</span></span>

[brew]: http://brew.sh/

## <a name="installation-of-latest-preview-release-via-homebrew-on-macos-1012-or-higher"></a><span data-ttu-id="4a047-116">macOS 10.12 이상에서 Homebrew를 통해 최신 미리 보기 릴리스 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-116">Installation of latest preview release via Homebrew on macOS 10.12 or higher</span></span>

<span data-ttu-id="4a047-117">Brew에 대한 자세한 내용은 [Brew정보](#about-brew)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a047-117">See [About Brew](#about-brew) for information about Brew.</span></span>

<span data-ttu-id="4a047-118">Homebrew를 설치했으면 PowerShell을 쉽게 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-118">Once you've installed Homebrew, installing PowerShell is easy.</span></span>
<span data-ttu-id="4a047-119">먼저, Cask 패키지의 다른 버전을 설치할 수 있는 [Cask-버전][cask-versions]을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-119">First, install [Cask-Versions][cask-versions] which lets you install alternative versions of cask packages:</span></span>

```sh
brew tap homebrew/cask-versions
```

<span data-ttu-id="4a047-120">이제 PowerShell을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-120">Now, you can install PowerShell:</span></span>

```sh
brew cask install powershell-preview
```

<span data-ttu-id="4a047-121">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-121">Finally, verify that your install is working properly:</span></span>

```sh
pwsh-preview
```

<span data-ttu-id="4a047-122">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-122">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> <span data-ttu-id="4a047-123">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만, 업그레이드를 완료하기 위해 PowerShell 셸을 종료하고 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-123">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade.</span></span>
> <span data-ttu-id="4a047-124">$PSVersionTable에 표시된 값을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-124">and refresh the values shown in $PSVersionTable.</span></span>

## <a name="installation-via-direct-download"></a><span data-ttu-id="4a047-125">직접 다운로드를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-125">Installation via Direct Download</span></span>

<span data-ttu-id="4a047-126">PKG 패키지 `powershell-6.1.0-osx-x64.pkg`를</span><span class="sxs-lookup"><span data-stu-id="4a047-126">Download the PKG package `powershell-6.1.0-osx-x64.pkg`</span></span>
<span data-ttu-id="4a047-127">[릴리스][] 페이지에서 macOS 머신으로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-127">from the [releases][] page onto your macOS machine.</span></span>

<span data-ttu-id="4a047-128">파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-128">You can double-click the file and follow the prompts, or install it from the terminal:</span></span>

```sh
sudo installer -pkg powershell-6.1.0-osx-x64.pkg -target /
```

<span data-ttu-id="4a047-129">[OpenSSL](#install-openssl)을 설치합니다. 이것은 PowerShell 원격 기능과 CIM 작업에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-129">Install [OpenSSL](#install-openssl) as this is needed for PowerShell remoting and CIM operations.</span></span>

## <a name="binary-archives"></a><span data-ttu-id="4a047-130">이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="4a047-130">Binary Archives</span></span>

<span data-ttu-id="4a047-131">고급 배포 시나리오를 사용하도록 설정하려면 macOS 플랫폼에 대해 PowerShell 이진 `tar.gz` 보관이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-131">PowerShell binary `tar.gz` archives are provided for the macOS platform to enable advanced deployment scenarios.</span></span>

### <a name="installing-binary-archives-on-macos"></a><span data-ttu-id="4a047-132">macOS에서 이진 보관 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-132">Installing binary archives on macOS</span></span>

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

<span data-ttu-id="4a047-133">[OpenSSL](#install-openssl)을 설치합니다. 이것은 PowerShell 원격 기능과 CIM 작업에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-133">Install [OpenSSL](#install-openssl) as this is needed for PowerShell remoting and CIM operations.</span></span>

## <a name="installing-dependencies"></a><span data-ttu-id="4a047-134">종속성 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-134">Installing dependencies</span></span>

### <a name="install-xcode-command-line-tools"></a><span data-ttu-id="4a047-135">XCode 명령줄 도구를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-135">Install XCode command line tools</span></span>

```shell
xcode-select -install
```

### <a name="install-openssl"></a><span data-ttu-id="4a047-136">OpenSSL 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-136">Install OpenSSL</span></span>

<span data-ttu-id="4a047-137">OpenSSL은 PowerShell 원격 기능 및 CIM 작업에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-137">OpenSSL is needed for PowerShell remoting and CIM operations.</span></span>  <span data-ttu-id="4a047-138">MacPorts 또는 Brew를 통해 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-138">You can install via MacPorts or Brew.</span></span>

#### <a name="install-openssl-via-brew"></a><span data-ttu-id="4a047-139">Brew를 통해 OpenSSL 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-139">Install OpenSSL via Brew</span></span>

<span data-ttu-id="4a047-140">Brew에 대한 자세한 내용은 [Brew정보](#about-brew)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a047-140">See [About Brew](#about-brew) for information about Brew.</span></span>

<span data-ttu-id="4a047-141">`brew install openssl`을 실행하여 OpenSSL을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-141">Run `brew install openssl` to install OpenSSL.</span></span>

#### <a name="install-openssl-via-macports"></a><span data-ttu-id="4a047-142">MacPorts를 통해 OpenSSL 설치</span><span class="sxs-lookup"><span data-stu-id="4a047-142">Install OpenSSL via MacPorts</span></span>

1. <span data-ttu-id="4a047-143">[XCode 명령줄 도구](#install-xcode-command-line-tools)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-143">Instal the [XCode command line tools](#install-xcode-command-line-tools)</span></span>
1. <span data-ttu-id="4a047-144">MacPorts를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-144">Install MacPorts.</span></span>
   <span data-ttu-id="4a047-145">도움이 필요하면 [설치 지침](https://guide.macports.org/chunked/installing.macports.html)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a047-145">See the [installation guide](https://guide.macports.org/chunked/installing.macports.html) if you need instructions.</span></span>
1. <span data-ttu-id="4a047-146">`sudo port selfupdate`를 실행하여 MacPorts 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-146">Update MacPorts by running `sudo port selfupdate`</span></span>
1. <span data-ttu-id="4a047-147">`sudo port upgrade outdated`를 실행하여 MacPorts 패키지를 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-147">Upgrade MacPorts packages by running `sudo port upgrade outdated`</span></span>
1. <span data-ttu-id="4a047-148">`sudo port instal openssl`을 실행하여 OpenSSL을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-148">Install OpenSSL by running by running `sudo port instal openssl`</span></span>
1. <span data-ttu-id="4a047-149">PowerShell에서 사용할 수 있도록 라이브러리를 링크합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-149">Link the libraries so that PowerShell can use it.</span></span>

```shell
sudo mkdir -p /usr/local/opt/openssl
sudo ln -s /opt/local/lib /usr/local/opt/openssl/lib
```

## <a name="uninstalling-powershell-core"></a><span data-ttu-id="4a047-150">PowerShell Core 제거</span><span class="sxs-lookup"><span data-stu-id="4a047-150">Uninstalling PowerShell Core</span></span>

<span data-ttu-id="4a047-151">Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-151">If you installed PowerShell with Homebrew, uninstallation is easy:</span></span>

```sh
brew cask uninstall powershell
```

<span data-ttu-id="4a047-152">직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-152">If you installed PowerShell via direct download, PowerShell must be removed manually:</span></span>

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

<span data-ttu-id="4a047-153">추가 PowerShell 경로를 제거하려면 이 문서의 [경로](#paths) 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-153">To remove the additional PowerShell paths, please see the [paths](#paths) section in this document and remove the desired the paths using `sudo rm`.</span></span>

> [!NOTE]
> <span data-ttu-id="4a047-154">Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-154">This is not necessary if you installed with Homebrew.</span></span>

## <a name="paths"></a><span data-ttu-id="4a047-155">경로</span><span class="sxs-lookup"><span data-stu-id="4a047-155">Paths</span></span>

* <span data-ttu-id="4a047-156">`$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`입니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-156">`$PSHOME` is `/usr/local/microsoft/powershell/6.1.0/`</span></span>
* <span data-ttu-id="4a047-157">사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-157">User profiles will be read from `~/.config/powershell/profile.ps1`</span></span>
* <span data-ttu-id="4a047-158">기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-158">Default profiles will be read from `$PSHOME/profile.ps1`</span></span>
* <span data-ttu-id="4a047-159">사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-159">User modules will be read from `~/.local/share/powershell/Modules`</span></span>
* <span data-ttu-id="4a047-160">공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-160">Shared modules will be read from `/usr/local/share/powershell/Modules`</span></span>
* <span data-ttu-id="4a047-161">기본 모듈은 `$PSHOME/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-161">Default modules will be read from `$PSHOME/Modules`</span></span>
* <span data-ttu-id="4a047-162">PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-162">PSReadline history will be recorded to `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`</span></span>

<span data-ttu-id="4a047-163">프로필은 PowerShell의 호스트별 구성을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-163">The profiles respect PowerShell's per-host configuration.</span></span>
<span data-ttu-id="4a047-164">따라서 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-164">So the default host-specific profiles exists at `Microsoft.PowerShell_profile.ps1` in the same locations.</span></span>

<span data-ttu-id="4a047-165">PowerShell은 macOS의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-165">PowerShell respects the [XDG Base Directory Specification][xdg-bds] on macOS.</span></span>

<span data-ttu-id="4a047-166">macOS는 BSD에서 파생된 것이므로 `/opt` 대신 `/usr/local`이 접두사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-166">Because macOS is a derivation of BSD, the prefix `/usr/local` is used instead of `/opt`.</span></span>
<span data-ttu-id="4a047-167">따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`이며 기호화된 링크는 `/usr/local/bin/pwsh`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a047-167">Thus, `$PSHOME` is `/usr/local/microsoft/powershell/6.1.0/`, and the symbolic link is placed at `/usr/local/bin/pwsh`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a047-168">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="4a047-168">Additional Resources</span></span>

* <span data-ttu-id="4a047-169">[Homebrew 웹][brew]</span><span class="sxs-lookup"><span data-stu-id="4a047-169">[Homebrew Web][brew]</span></span>
* <span data-ttu-id="4a047-170">[Homebrew Github 리포지토리][GitHub]</span><span class="sxs-lookup"><span data-stu-id="4a047-170">[Homebrew Github Repository][GitHub]</span></span>
* <span data-ttu-id="4a047-171">[Homebrew-Cask][cask]</span><span class="sxs-lookup"><span data-stu-id="4a047-171">[Homebrew-Cask][cask]</span></span>

[brew]: http://brew.sh/
[Cask]: https://github.com/Homebrew/homebrew-cask
[cask-versions]: https://github.com/Homebrew/homebrew-cask-versions
[GitHub]: https://github.com/Homebrew
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[releases]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
