# <a name="installing-powershell-core-on-macos"></a><span data-ttu-id="f4a84-101">macOS에서 PowerShell Core 설치</span><span class="sxs-lookup"><span data-stu-id="f4a84-101">Installing PowerShell Core on macOS</span></span>

<span data-ttu-id="f4a84-102">PowerShell Core는 macOS 10.12 이상을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-102">PowerShell Core supports macOS 10.12 and higher.</span></span>
<span data-ttu-id="f4a84-103">모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-103">All packages are available on our GitHub [releases][] page.</span></span>
<span data-ttu-id="f4a84-104">패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-104">Once the package is installed, run `pwsh` from a terminal.</span></span>

### <a name="installation-via-homebrew-on-macos-1012"></a><span data-ttu-id="f4a84-105">macOS 10.12 이상에서 Homebrew를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="f4a84-105">Installation via Homebrew on macOS 10.12+</span></span>

<span data-ttu-id="f4a84-106">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-106">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="f4a84-107">터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-107">From a terminal window, type `brew` to run Homebrew.</span></span>  <span data-ttu-id="f4a84-108">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-108">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

> [!NOTE]
> <span data-ttu-id="f4a84-109">이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-109">If you installed Homebrew in the past, it's always a good idea to run 'brew update-reset' && 'brew update'.</span></span>
```sh
brew update-reset
brew update
```

> <span data-ttu-id="f4a84-110">Homebrew의 이전 버전에서는 ‘caskroom/cask’를 사용했으나, 더 이상 사용되지 않고 ‘homebrew/cask’로 마이그레이션되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-110">Older versions of Homebrew used the tap 'caskroom/cask', which has been deprecated, and migrated into 'homebrew/cask'.</span></span>  <span data-ttu-id="f4a84-111">자세한 내용은 [Homebrew-cask][cask]를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4a84-111">More information can be found at [Homebrew-cask][cask].</span></span> <span data-ttu-id="f4a84-112">‘brew tap’ 명령을 사용하여 현재 탭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-112">Use the 'brew tap' command to list your current taps.</span></span>  <span data-ttu-id="f4a84-113">‘caskroom/cask’가 표시되면 ‘brew update’를 사용하여 Homebrew가 탭을 마이그레이션하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-113">If you see 'caskroom/cask' you can use 'brew update' to have Homebrew migrate the taps.</span></span>

```sh
brew tap
brew update
```

<span data-ttu-id="f4a84-114">Homebrew를 설치/업데이트한 후 PowerShell을 쉽게 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-114">Once you've installed/updated Homebrew, installing PowerShell is easy.</span></span>

<span data-ttu-id="f4a84-115">PowerShell을 설치하려면</span><span class="sxs-lookup"><span data-stu-id="f4a84-115">To install PowerShell:</span></span>

```sh
brew cask install powershell
```

<span data-ttu-id="f4a84-116">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-116">Finally, verify that your install is working properly:</span></span>

```sh
pwsh
```

<span data-ttu-id="f4a84-117">PowerShell을 종료하고 bash로 돌아가려면 ‘exit’ 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-117">To exit PowerShell, and return to bash, use the 'exit' command.</span></span> 
```sh
exit
```

<span data-ttu-id="f4a84-118">PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-118">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell:</span></span>

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> <span data-ttu-id="f4a84-119">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-119">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade and refresh the values shown in $PSVersionTable.</span></span>

### <a name="installing-preview-via-homebrew-on-macos-1012"></a><span data-ttu-id="f4a84-120">macOS 10.12 이상에서 Homebrew를 통해 미리 보기 설치</span><span class="sxs-lookup"><span data-stu-id="f4a84-120">Installing Preview via Homebrew on macOS 10.12+</span></span>

<span data-ttu-id="f4a84-121">[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-121">[Homebrew][brew] is the preferred package manager for macOS.</span></span>
<span data-ttu-id="f4a84-122">터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-122">From a terminal window, type `brew` to run Homebrew.</span></span>  <span data-ttu-id="f4a84-123">`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-123">If the `brew` command is not found, you need to install Homebrew following [their instructions][brew].</span></span>

> [!NOTE]
> <span data-ttu-id="f4a84-124">이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-124">If you installed Homebrew in the past, it's always a good idea to run 'brew update-reset' && 'brew update'.</span></span>
```sh
brew update-reset
brew update
```

<span data-ttu-id="f4a84-125">그런 다음, 미리 보기 패키지를 가져오려면 `versions` casks 리포지토리를 탭해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-125">Then, you must tap the `versions` casks repository to get the preview package:</span></span>

```sh
brew tap homebrew/cask-versions
```

<span data-ttu-id="f4a84-126">PowerShell 미리 보기를 설치하려면:</span><span class="sxs-lookup"><span data-stu-id="f4a84-126">To install PowerShell Preview:</span></span>

```sh
brew cask install powershell-preview
```

<span data-ttu-id="f4a84-127">최종적으로, 설치가 제대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-127">Finally, verify that your install is working properly:</span></span>

```sh
pwsh-preview
```

<span data-ttu-id="f4a84-128">PowerShell의 새 버전이 릴리스되면 Homebrew의 수식을 업데이트하고 PowerShell 미리 보기를 업그레이드하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-128">When new versions of PowerShell are released, simply update Homebrew's formulae and upgrade PowerShell Preview:</span></span>

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> <span data-ttu-id="f4a84-129">위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-129">The commands above can be called from within a PowerShell (pwsh) host, but then the PowerShell shell must be exited and restarted to complete the upgrade and refresh the values shown in $PSVersionTable.</span></span>

### <a name="installation-via-direct-download"></a><span data-ttu-id="f4a84-130">직접 다운로드를 통해 설치</span><span class="sxs-lookup"><span data-stu-id="f4a84-130">Installation via Direct Download</span></span>

<span data-ttu-id="f4a84-131">[릴리스][] 페이지의 PKG 패키지 `powershell-6.0.2-osx.10.12-x64.pkg`를 macOS 컴퓨터로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-131">Download the PKG package `powershell-6.0.2-osx.10.12-x64.pkg` from the [releases][] page onto your macOS machine.</span></span>

<span data-ttu-id="f4a84-132">파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-132">You can double-click the file and follow the prompts, or install it from the terminal:</span></span>

```sh
sudo installer -pkg powershell-6.0.2-osx.10.12-x64.pkg -target /
```

## <a name="binary-archives"></a><span data-ttu-id="f4a84-133">이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="f4a84-133">Binary Archives</span></span>

<span data-ttu-id="f4a84-134">고급 배포 시나리오를 지원하기 위해 macOS 및 Linux 플랫폼에 PowerShell 이진 `tar.gz` 아카이브가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-134">PowerShell binary `tar.gz` archives are provided for macOS and Linux platforms to enable advanced deployment scenarios.</span></span>

### <a name="installing-binary-archives-on-macos"></a><span data-ttu-id="f4a84-135">macOS에서 이진 보관 설치</span><span class="sxs-lookup"><span data-stu-id="f4a84-135">Installing binary archives on macOS</span></span>

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

## <a name="uninstalling-powershell-core"></a><span data-ttu-id="f4a84-136">PowerShell Core 제거</span><span class="sxs-lookup"><span data-stu-id="f4a84-136">Uninstalling PowerShell Core</span></span>

<span data-ttu-id="f4a84-137">Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-137">If you installed PowerShell with Homebrew, uninstallation is easy:</span></span>

```sh
brew cask uninstall powershell
```

<span data-ttu-id="f4a84-138">직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-138">If you installed PowerShell via direct download, PowerShell must be removed manually:</span></span>

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

<span data-ttu-id="f4a84-139">추가 PowerShell 경로를 제거하려면 이 문서의 [경로][] 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-139">To remove the additional PowerShell paths, please see the [paths][] section in this document and remove the desired the paths using `sudo rm`.</span></span>

> [!NOTE]
> <span data-ttu-id="f4a84-140">Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-140">This is not necessary if you installed with Homebrew.</span></span>

[경로]:#paths
[paths]:#paths

## <a name="paths"></a><span data-ttu-id="f4a84-142">경로</span><span class="sxs-lookup"><span data-stu-id="f4a84-142">Paths</span></span>

* <span data-ttu-id="f4a84-143">`$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`입니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-143">`$PSHOME` is `/usr/local/microsoft/powershell/6.0.2/`</span></span>
* <span data-ttu-id="f4a84-144">사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-144">User profiles will be read from `~/.config/powershell/profile.ps1`</span></span>
* <span data-ttu-id="f4a84-145">기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-145">Default profiles will be read from `$PSHOME/profile.ps1`</span></span>
* <span data-ttu-id="f4a84-146">사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-146">User modules will be read from `~/.local/share/powershell/Modules`</span></span>
* <span data-ttu-id="f4a84-147">공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-147">Shared modules will be read from `/usr/local/share/powershell/Modules`</span></span>
* <span data-ttu-id="f4a84-148">기본 모듈은 `$PSHOME/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-148">Default modules will be read from `$PSHOME/Modules`</span></span>
* <span data-ttu-id="f4a84-149">PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-149">PSReadline history will be recorded to `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`</span></span>

<span data-ttu-id="f4a84-150">프로필은 PowerShell의 호스트별 구성을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-150">The profiles respect PowerShell's per-host configuration.</span></span>
<span data-ttu-id="f4a84-151">따라서 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-151">So the default host-specific profiles exists at `Microsoft.PowerShell_profile.ps1` in the same locations.</span></span>

<span data-ttu-id="f4a84-152">PowerShell은 macOS의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-152">PowerShell respects the [XDG Base Directory Specification][xdg-bds] on macOS.</span></span>

<span data-ttu-id="f4a84-153">macOS는 BSD에서 파생된 것이므로 `/opt` 대신 `/usr/local`이 접두사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-153">Because macOS is a derivation of BSD, the prefix `/usr/local` is used instead of `/opt`.</span></span>
<span data-ttu-id="f4a84-154">따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`이며 symlink는 `/usr/local/bin/pwsh`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a84-154">Thus, `$PSHOME` is `/usr/local/microsoft/powershell/6.0.2/`, and the symlink is placed at `/usr/local/bin/pwsh`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4a84-155">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="f4a84-155">Additional Resources</span></span>

* <span data-ttu-id="f4a84-156">[Homebrew 웹][brew]</span><span class="sxs-lookup"><span data-stu-id="f4a84-156">[Homebrew Web][brew]</span></span>
* <span data-ttu-id="f4a84-157">[Homebrew Github 리포지토리][GitHub]</span><span class="sxs-lookup"><span data-stu-id="f4a84-157">[Homebrew Github Repository][GitHub]</span></span>
* <span data-ttu-id="f4a84-158">[Homebrew-Cask][cask]</span><span class="sxs-lookup"><span data-stu-id="f4a84-158">[Homebrew-Cask][cask]</span></span>


[brew]: http://brew.sh/
[GitHub]: https://github.com/Homebrew
[Cask]: https://github.com/Homebrew/homebrew-cask
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[releases]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
