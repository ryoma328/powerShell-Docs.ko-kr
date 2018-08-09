---
title: Linux에서 PowerShell Core 설치
description: 다양한 Linux 배포판에서 PowerShell Core를 설치하는 방법에 대한 정보
ms.date: 08/06/2018
ms.openlocfilehash: a6b0e3003f84ea6dc99cffcc7edf1b5b6963aa21
ms.sourcegitcommit: 01ac77cd0b00e4e5e964504563a9212e8002e5e0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2018
ms.locfileid: "39587451"
---
# <a name="installing-powershell-core-on-linux"></a><span data-ttu-id="e80ae-103">Linux에서 PowerShell Core 설치</span><span class="sxs-lookup"><span data-stu-id="e80ae-103">Installing PowerShell Core on Linux</span></span>

<span data-ttu-id="e80ae-104">[Ubuntu 14.04][u14], [Ubuntu 16.04][u16], [Ubuntu 18.10][u18], [Debian 8][deb8], [Debian 9][deb9], [CentOS 7][cos], [Red Hat Enterprise Linux (RHEL) 7][rhel7], [OpenSUSE 42.3][opensuse], [Fedora 27][fedora], [Fedora 28][fedora] 및 [Arch Linux][arch]를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-104">Supports [Ubuntu 14.04][u14], [Ubuntu 16.04][u16], [Ubuntu 18.10][u18], [Debian 8][deb8], [Debian 9][deb9], [CentOS 7][cos], [Red Hat Enterprise Linux (RHEL) 7][rhel7], [OpenSUSE 42.3][opensuse], [Fedora 27][fedora], [Fedora 28][fedora], and [Arch Linux][arch].</span></span>

<span data-ttu-id="e80ae-105">공식적으로 지원되지 않는 Linux 배포의 경우 [PowerShell 맞춤 패키지][snap]를 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="e80ae-105">For Linux distributions that are not officially supported, you can try using the [PowerShell Snap Package][snap].</span></span>
<span data-ttu-id="e80ae-106">또한 Linux [`tar.gz` 보관][tar]을 사용하여 PowerShell 이진 파일을 직접 배포해 볼 수도 있지만 OS에 따라 별도의 단계로 필요한 종속성을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-106">You can also try deploying PowerShell binaries directly using the Linux [`tar.gz` archive][tar], but you would need to set up the necessary dependencies based on the OS in separate steps.</span></span>

<span data-ttu-id="e80ae-107">모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-107">All packages are available on our GitHub [releases][] page.</span></span>
<span data-ttu-id="e80ae-108">패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-108">Once the package is installed, run `pwsh` from a terminal.</span></span>

[u14]: #ubuntu-1404
[u16]: #ubuntu-1604
[u18]: #ubuntu-1810
[u18]: #ubuntu-1804
[deb8]: #debian-8
[deb9]: #debian-9
[cos]: #centos-7
[rhel7]: #red-hat-enterprise-linux-rhel-7
[opensuse]: #opensuse-423
[fedora]: #fedora
[arch]: #arch-linux
[snap]: #snap-package
[tar]: #binary-archives

## <a name="installing-preview-releases"></a><span data-ttu-id="e80ae-109">미리 보기 릴리스 설치</span><span class="sxs-lookup"><span data-stu-id="e80ae-109">Installing Preview Releases</span></span>

<span data-ttu-id="e80ae-110">패키지 리포지토리를 통해 Linux용 PowerShell Core 미리 보기 릴리스를 설치할 때 패키지 이름을 `powershell`에서 `powershell-preview`로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-110">When installing a PowerShell Core Preview release for Linux via a Package Repository, the package name changes from `powershell` to `powershell-preview`.</span></span>

<span data-ttu-id="e80ae-111">직접 다운로드를 통한 설치는 파일 이름 외에는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-111">Installing via direct download does not change, other than the file name.</span></span>

<span data-ttu-id="e80ae-112">다양한 패키지 관리자를 사용하여 안정적인 미리 보기 패키지를 설치하는 명령의 테이블은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-112">Here is a table of the commands to install the stable and preview packages using the various package managers:</span></span>

|<span data-ttu-id="e80ae-113">배포</span><span class="sxs-lookup"><span data-stu-id="e80ae-113">Distribution(s)</span></span>|<span data-ttu-id="e80ae-114">안정적인 명령</span><span class="sxs-lookup"><span data-stu-id="e80ae-114">Stable Command</span></span> | <span data-ttu-id="e80ae-115">미리 보기 명령</span><span class="sxs-lookup"><span data-stu-id="e80ae-115">Preview Command</span></span> |
|---------------|---------------|-----------------|
| <span data-ttu-id="e80ae-116">Ubuntu, Debian</span><span class="sxs-lookup"><span data-stu-id="e80ae-116">Ubuntu, Debian</span></span> |`sudo apt-get install -y powershell`| `sudo apt-get install -y powershell-preview`|
| <span data-ttu-id="e80ae-117">CentOS, RedHat</span><span class="sxs-lookup"><span data-stu-id="e80ae-117">CentOS, RedHat</span></span> |`sudo yum install -y powershell` | `sudo yum install -y powershell-preview`|
| <span data-ttu-id="e80ae-118">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="e80ae-118">OpenSUSE</span></span> |`sudo zypper install powershell` | `sudo zypper install powershell-preview`|
| <span data-ttu-id="e80ae-119">Fedora</span><span class="sxs-lookup"><span data-stu-id="e80ae-119">Fedora</span></span>   |`sudo dnf install -y powershell` | `sudo dnf install -y powershell-preview`|

## <a name="ubuntu-1404"></a><span data-ttu-id="e80ae-120">Ubuntu 14.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-120">Ubuntu 14.04</span></span>

### <a name="installation-via-package-repository---ubuntu-1404"></a><span data-ttu-id="e80ae-121">패키지 리포지토리를 통해 설치 - Ubuntu 14.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-121">Installation via Package Repository - Ubuntu 14.04</span></span>

<span data-ttu-id="e80ae-122">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 패키지 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-122">PowerShell Core, for Linux, is published to package repositories for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-123">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-123">This is the preferred method.</span></span>

```sh
# Import the public repository GPG keys
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# Register the Microsoft Ubuntu repository
curl https://packages.microsoft.com/config/ubuntu/14.04/prod.list | sudo tee /etc/apt/sources.list.d/microsoft.list

# Update the list of products
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-124">슈퍼 사용자로 Microsoft 리포지토리를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-124">As superuser, register the Microsoft repository.</span></span>
<span data-ttu-id="e80ae-125">그 이후에는 `sudo apt-get upgrade powershell`을 사용하여 설치를 업데이트하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-125">From then on, you just need to use `sudo apt-get upgrade powershell` to update the installation.</span></span>

### <a name="installation-via-direct-download---ubuntu-1404"></a><span data-ttu-id="e80ae-126">직접 다운로드를 통해 설치 - Ubuntu 14.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-126">Installation via Direct Download - Ubuntu 14.04</span></span>

<span data-ttu-id="e80ae-127">[릴리스][] 페이지의 Debian 패키지 `powershell_6.0.2-1.ubuntu.14.04_amd64.deb`를 Ubuntu 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-127">Download the Debian package `powershell_6.0.2-1.ubuntu.14.04_amd64.deb` from the [releases][] page onto the Ubuntu machine.</span></span>

<span data-ttu-id="e80ae-128">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-128">Then execute the following in the terminal:</span></span>

```sh
sudo dpkg -i powershell_6.0.2-1.ubuntu.14.04_amd64.deb
sudo apt-get install -f
```

> [!NOTE]
> <span data-ttu-id="e80ae-129">`dpkg -i` 명령은 충족되지 않은 종속성으로 인해 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-129">The `dpkg -i` command fails with unmet dependencies.</span></span>
> <span data-ttu-id="e80ae-130">다음 명령인 `apt-get install -f`는 이러한 문제를 해결한 다음, PowerShell 패키지 구성을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-130">The next command, `apt-get install -f` resolves these issues then finishes configuring the PowerShell package.</span></span>

### <a name="uninstallation---ubuntu-1404"></a><span data-ttu-id="e80ae-131">제거 - Ubuntu 14.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-131">Uninstallation - Ubuntu 14.04</span></span>

```sh
sudo apt-get remove powershell
```

## <a name="ubuntu-1604"></a><span data-ttu-id="e80ae-132">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-132">Ubuntu 16.04</span></span>

### <a name="installation-via-package-repository---ubuntu-1604"></a><span data-ttu-id="e80ae-133">패키지 리포지토리를 통해 설치 - Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-133">Installation via Package Repository - Ubuntu 16.04</span></span>

<span data-ttu-id="e80ae-134">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 패키지 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-134">PowerShell Core, for Linux, is published to package repositories for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-135">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-135">This is the preferred method.</span></span>

```sh
# Import the public repository GPG keys
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# Register the Microsoft Ubuntu repository
sudo curl -o /etc/apt/sources.list.d/microsoft.list https://packages.microsoft.com/config/ubuntu/16.04/prod.list

# Update the list of products
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-136">Microsoft 리포지토리를 superuser로 등록하고 나면 그 이후부터는 `sudo apt-get upgrade powershell`을 사용하여 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-136">After registering the Microsoft repository once as superuser, from then on, you just need to use `sudo apt-get upgrade powershell` to update it.</span></span>

### <a name="installation-via-direct-download---ubuntu-1604"></a><span data-ttu-id="e80ae-137">직접 다운로드를 통해 설치 - Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-137">Installation via Direct Download - Ubuntu 16.04</span></span>

<span data-ttu-id="e80ae-138">[릴리스][] 페이지의 Debian 패키지 `powershell_6.0.2-1.ubuntu.16.04_amd64.deb`를 Ubuntu 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-138">Download the Debian package `powershell_6.0.2-1.ubuntu.16.04_amd64.deb` from the [releases][] page onto the Ubuntu machine.</span></span>

<span data-ttu-id="e80ae-139">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-139">Then execute the following in the terminal:</span></span>

```sh
sudo dpkg -i powershell_6.0.2-1.ubuntu.16.04_amd64.deb
sudo apt-get install -f
```

> [!NOTE]
> <span data-ttu-id="e80ae-140">`dpkg -i` 명령은 충족되지 않은 종속성으로 인해 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-140">The `dpkg -i` command fails with unmet dependencies.</span></span>
> <span data-ttu-id="e80ae-141">다음 명령인 `apt-get install -f`는 이러한 문제를 해결한 다음, PowerShell 패키지 구성을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-141">The next command, `apt-get install -f` resolves these issues then finishes configuring the PowerShell package.</span></span>

### <a name="uninstallation---ubuntu-1604"></a><span data-ttu-id="e80ae-142">제거 - Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-142">Uninstallation - Ubuntu 16.04</span></span>

```sh
sudo apt-get remove powershell
```

## <a name="ubuntu-1804"></a><span data-ttu-id="e80ae-143">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-143">Ubuntu 18.04</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-144">Ubuntu 18.04에 대한 지원이 `6.1.0-preview.2` 이후에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-144">Support for Ubuntu 18.04 was added after `6.1.0-preview.2`</span></span>

### <a name="installation-via-package-repository---ubuntu-1804"></a><span data-ttu-id="e80ae-145">패키지 리포지토리를 통해 설치 - Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-145">Installation via Package Repository - Ubuntu 18.04</span></span>

<span data-ttu-id="e80ae-146">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 패키지 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-146">PowerShell Core, for Linux, is published to package repositories for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-147">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-147">This is the preferred method.</span></span>

```sh
# Import the public repository GPG keys
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# Register the Microsoft Ubuntu repository
sudo curl -o /etc/apt/sources.list.d/microsoft.list https://packages.microsoft.com/config/ubuntu/18.04/prod.list

# Update the list of products
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell-preview

# Start PowerShell
pwsh-preview
```

<span data-ttu-id="e80ae-148">Microsoft 리포지토리를 superuser로 등록하고 나면 그 이후부터는 `sudo apt-get upgrade powershell`을 사용하여 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-148">After registering the Microsoft repository once as superuser, from then on, you just need to use `sudo apt-get upgrade powershell` to update it.</span></span>

### <a name="installation-via-direct-download---ubuntu-1804"></a><span data-ttu-id="e80ae-149">직접 다운로드를 통해 설치 - Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-149">Installation via Direct Download - Ubuntu 18.04</span></span>

<span data-ttu-id="e80ae-150">[릴리스][] 페이지의 Debian 패키지 `powershell_6.1.0-preview.3-1.ubuntu.18.04_amd64.deb`를 Ubuntu 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-150">Download the Debian package `powershell_6.1.0-preview.3-1.ubuntu.18.04_amd64.deb` from the [releases][] page onto the Ubuntu machine.</span></span>

<span data-ttu-id="e80ae-151">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-151">Then execute the following in the terminal:</span></span>

```sh
sudo dpkg -i powershell_6.1.0-preview.3-1.ubuntu.18.04_amd64.deb
sudo apt-get install -f
```

> [!NOTE]
> <span data-ttu-id="e80ae-152">`dpkg -i` 명령은 충족되지 않은 종속성으로 인해 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-152">The `dpkg -i` command fails with unmet dependencies.</span></span>
> <span data-ttu-id="e80ae-153">다음 명령인 `apt-get install -f`는 이러한 문제를 해결한 다음, PowerShell 패키지 구성을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-153">The next command, `apt-get install -f` resolves these issues then finishes configuring the PowerShell package.</span></span>

### <a name="uninstallation---ubuntu-1804"></a><span data-ttu-id="e80ae-154">제거 - Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-154">Uninstallation - Ubuntu 18.04</span></span>

```sh
sudo apt-get remove powershell
```

## <a name="ubuntu-1810"></a><span data-ttu-id="e80ae-155">Ubuntu 18.10</span><span class="sxs-lookup"><span data-stu-id="e80ae-155">Ubuntu 18.10</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-156">Ubuntu 18.10에 대한 지원이 `6.1.0-preview.3` 이후에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-156">Support for Ubuntu 18.10 was added after `6.1.0-preview.3`.</span></span>
> <span data-ttu-id="e80ae-157">18.10은 일일 빌드이므로 커뮤니티에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-157">As 18.10 is a daily build, it is only community supported.</span></span>

<span data-ttu-id="e80ae-158">18.10의 설치는 `snapd`를 통해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-158">Installing on 18.10 is supported via `snapd`.</span></span> <span data-ttu-id="e80ae-159">전체 지침은 [맞춤 패키지][snap]를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e80ae-159">See [Snap Package][snap] for full instructions;</span></span>

## <a name="debian-8"></a><span data-ttu-id="e80ae-160">Debian 8</span><span class="sxs-lookup"><span data-stu-id="e80ae-160">Debian 8</span></span>

### <a name="installation-via-package-repository---debian-8"></a><span data-ttu-id="e80ae-161">패키지 리포지토리를 통해 설치 - Debian 8</span><span class="sxs-lookup"><span data-stu-id="e80ae-161">Installation via Package Repository - Debian 8</span></span>

<span data-ttu-id="e80ae-162">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 패키지 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-162">PowerShell Core, for Linux, is published to package repositories for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-163">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-163">This is the preferred method.</span></span>

```sh
# Install system components
sudo apt-get update
sudo apt-get install curl apt-transport-https

# Import the public repository GPG keys
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# Register the Microsoft Product feed
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-jessie-prod jessie main" > /etc/apt/sources.list.d/microsoft.list'

# Update the list of products
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-164">Microsoft 리포지토리를 superuser로 등록하고 나면 그 이후부터는 `sudo apt-get upgrade powershell`을 사용하여 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-164">After registering the Microsoft repository once as superuser, from then on, you just need to use `sudo apt-get upgrade powershell` to update it.</span></span>

### <a name="installation-via-direct-download---debian-8"></a><span data-ttu-id="e80ae-165">직접 다운로드를 통해 설치 - Debian 8</span><span class="sxs-lookup"><span data-stu-id="e80ae-165">Installation via Direct Download - Debian 8</span></span>

<span data-ttu-id="e80ae-166">[릴리스][] 페이지의 Debian 패키지 `powershell_6.0.2-1.debian.8_amd64.deb`를 Debian 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-166">Download the Debian package `powershell_6.0.2-1.debian.8_amd64.deb` from the [releases][] page onto the Debian machine.</span></span>

<span data-ttu-id="e80ae-167">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-167">Then execute the following in the terminal:</span></span>

```sh
sudo dpkg -i powershell_6.0.2-1.debian.8_amd64.deb
sudo apt-get install -f
```

> [!NOTE]
> <span data-ttu-id="e80ae-168">`dpkg -i` 명령은 충족되지 않은 종속성으로 인해 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-168">The `dpkg -i` command fails with unmet dependencies.</span></span>
> <span data-ttu-id="e80ae-169">다음 명령인 `apt-get install -f`는 이러한 문제를 해결한 다음, PowerShell 패키지 구성을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-169">The next command, `apt-get install -f` resolves these issues then finishes configuring the PowerShell package.</span></span>

### <a name="uninstallation---debian-8"></a><span data-ttu-id="e80ae-170">제거 - Debian 8</span><span class="sxs-lookup"><span data-stu-id="e80ae-170">Uninstallation - Debian 8</span></span>

```sh
sudo apt-get remove powershell
```

## <a name="debian-9"></a><span data-ttu-id="e80ae-171">Debian 9</span><span class="sxs-lookup"><span data-stu-id="e80ae-171">Debian 9</span></span>

### <a name="installation-via-package-repository---debian-9"></a><span data-ttu-id="e80ae-172">패키지 리포지토리를 통해 설치 - Debian 9</span><span class="sxs-lookup"><span data-stu-id="e80ae-172">Installation via Package Repository - Debian 9</span></span>

<span data-ttu-id="e80ae-173">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 패키지 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-173">PowerShell Core, for Linux, is published to package repositories for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-174">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-174">This is the preferred method.</span></span>

```sh
# Install system components
sudo apt-get update
sudo apt-get install curl gnupg apt-transport-https

# Import the public repository GPG keys
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# Register the Microsoft Product feed
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-stretch-prod stretch main" > /etc/apt/sources.list.d/microsoft.list'

# Update the list of products
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-175">Microsoft 리포지토리를 superuser로 등록하고 나면 그 이후부터는 `sudo apt-get upgrade powershell`을 사용하여 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-175">After registering the Microsoft repository once as superuser, from then on, you just need to use `sudo apt-get upgrade powershell` to update it.</span></span>

### <a name="installation-via-direct-download---debian-9"></a><span data-ttu-id="e80ae-176">직접 다운로드를 통해 설치 - Debian 9</span><span class="sxs-lookup"><span data-stu-id="e80ae-176">Installation via Direct Download - Debian 9</span></span>

<span data-ttu-id="e80ae-177">[릴리스][] 페이지의 Debian 패키지 `powershell_6.0.2-1.debian.9_amd64.deb`를 Debian 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-177">Download the Debian package `powershell_6.0.2-1.debian.9_amd64.deb` from the [releases][] page onto the Debian machine.</span></span>

<span data-ttu-id="e80ae-178">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-178">Then execute the following in the terminal:</span></span>

```sh
sudo dpkg -i powershell_6.0.2-1.debian.9_amd64.deb
sudo apt-get install -f
```

### <a name="uninstallation---debian-9"></a><span data-ttu-id="e80ae-179">제거 - Debian 9</span><span class="sxs-lookup"><span data-stu-id="e80ae-179">Uninstallation - Debian 9</span></span>

```sh
sudo apt-get remove powershell
```

## <a name="centos-7"></a><span data-ttu-id="e80ae-180">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-180">CentOS 7</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-181">이 패키지는 Oracle Linux 7에서도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-181">This package also works on Oracle Linux 7.</span></span>

### <a name="installation-via-package-repository-preferred---centos-7"></a><span data-ttu-id="e80ae-182">패키지 리포지토리를 통해 설치(권장) - CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-182">Installation via Package Repository (preferred) - CentOS 7</span></span>

<span data-ttu-id="e80ae-183">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 공식 Microsoft 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-183">PowerShell Core for Linux is published to official Microsoft repositories for easy installation (and updates).</span></span>

```sh
# Register the Microsoft RedHat repository
curl https://packages.microsoft.com/config/rhel/7/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo

# Install PowerShell
sudo yum install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-184">Microsoft 리포지토리를 superuser로 등록하고 나면 `sudo yum update powershell`을 사용하여 PowerShell을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-184">After registering the Microsoft repository once as superuser, you just need to use `sudo yum update powershell` to update PowerShell.</span></span>

### <a name="installation-via-direct-download---centos-7"></a><span data-ttu-id="e80ae-185">직접 다운로드를 통해 설치 - CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-185">Installation via Direct Download - CentOS 7</span></span>

<span data-ttu-id="e80ae-186">[CentOS 7][]을 사용하여 [릴리스][] 페이지의 RPM 패키지 `powershell-6.0.2-1.rhel.7.x86_64.rpm`을 CentOS 컴퓨터로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-186">Using [CentOS 7][], download the RPM package `powershell-6.0.2-1.rhel.7.x86_64.rpm` from the [releases][] page onto the CentOS machine.</span></span>

<span data-ttu-id="e80ae-187">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-187">Then execute the following in the terminal:</span></span>

```sh
sudo yum install powershell-6.0.2-1.rhel.7.x86_64.rpm
```

<span data-ttu-id="e80ae-188">또한 다운로드의 중간 단계 없이 RPM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-188">You can also install the RPM without the intermediate step of downloading it:</span></span>

```sh
sudo yum install https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-1.rhel.7.x86_64.rpm
```

### <a name="uninstallation---centos-7"></a><span data-ttu-id="e80ae-189">제거 - CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-189">Uninstallation - CentOS 7</span></span>

```sh
sudo yum remove powershell
```

[CentOS 7]: https://www.centos.org/download/

## <a name="red-hat-enterprise-linux-rhel-7"></a><span data-ttu-id="e80ae-191">Red Hat Enterprise Linux(RHEL) 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-191">Red Hat Enterprise Linux (RHEL) 7</span></span>

### <a name="installation-via-package-repository-preferred---red-hat-enterprise-linux-rhel-7"></a><span data-ttu-id="e80ae-192">패키지 리포지토리(권장)를 통해 설치 - Red Hat Enterprise Linux(RHEL) 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-192">Installation via Package Repository (preferred) - Red Hat Enterprise Linux (RHEL) 7</span></span>

<span data-ttu-id="e80ae-193">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 공식 Microsoft 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-193">PowerShell Core for Linux is published to official Microsoft repositories for easy installation (and updates).</span></span>

```sh
# Register the Microsoft RedHat repository
curl https://packages.microsoft.com/config/rhel/7/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo

# Install PowerShell
sudo yum install -y powershell

# Start PowerShell
pwsh
```

<span data-ttu-id="e80ae-194">Microsoft 리포지토리를 superuser로 등록하고 나면 `sudo yum update powershell`을 사용하여 PowerShell을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-194">After registering the Microsoft repository once as superuser, you just need to use `sudo yum update powershell` to update PowerShell.</span></span>

### <a name="installation-via-direct-download---red-hat-enterprise-linux-rhel-7"></a><span data-ttu-id="e80ae-195">직접 다운로드를 통해 설치 - Red Hat Enterprise Linux(RHEL) 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-195">Installation via Direct Download - Red Hat Enterprise Linux (RHEL) 7</span></span>

<span data-ttu-id="e80ae-196">[릴리스][] 페이지의 RPM 패키지 `powershell-6.0.2-1.rhel.7.x86_64.rpm`을 Red Hat Enterprise Linux 컴퓨터로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-196">Download the RPM package `powershell-6.0.2-1.rhel.7.x86_64.rpm` from the [releases][] page onto the Red Hat Enterprise Linux machine.</span></span>

<span data-ttu-id="e80ae-197">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-197">Then execute the following in the terminal:</span></span>

```sh
sudo yum install powershell-6.0.2-1.rhel.7.x86_64.rpm
```

<span data-ttu-id="e80ae-198">또한 다운로드의 중간 단계 없이 RPM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-198">You can also install the RPM without the intermediate step of downloading it:</span></span>

```sh
sudo yum install https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-1.rhel.7.x86_64.rpm
```

### <a name="uninstallation---red-hat-enterprise-linux-rhel-7"></a><span data-ttu-id="e80ae-199">제거 - Red Hat Enterprise Linux(RHEL) 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-199">Uninstallation - Red Hat Enterprise Linux (RHEL) 7</span></span>

```sh
sudo yum remove powershell
```

## <a name="opensuse-423"></a><span data-ttu-id="e80ae-200">OpenSUSE 42.3</span><span class="sxs-lookup"><span data-stu-id="e80ae-200">OpenSUSE 42.3</span></span>

<span data-ttu-id="e80ae-201">PowerShell Core를 설치할 때 `zypper`에서 다음 오류를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-201">When installing PowerShell Core, `zypper` may report the following error:</span></span>

```Output
Problem: nothing provides libcurl needed by powershell-6.0.1-1.rhel.7.x86_64
 Solution 1: do not install powershell-6.0.1-1.rhel.7.x86_64
 Solution 2: break powershell-6.0.1-1.rhel.7.x86_64 by ignoring some of its dependencies
```

<span data-ttu-id="e80ae-202">이 경우 다음 명령이 설치된 대로 `libcurl4` 패키지를 보여 주는지 확인하여 호환되는 `libcurl` 라이브러리가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-202">In this case, verify that a compatible `libcurl` library is present by checking that the following command shows the `libcurl4` package as installed:</span></span>

```sh
zypper search --file-list --match-exact '/usr/lib64/libcurl.so.4'
```

<span data-ttu-id="e80ae-203">그런 다음, PowerShell 패키지를 설치할 때 `break powershell-6.0.1-1.rhel.7.x86_64 by ignoring some of its dependencies` 솔루션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-203">Then choose the `break powershell-6.0.1-1.rhel.7.x86_64 by ignoring some of its dependencies` solution when installing the PowerShell package.</span></span>

### <a name="installation-via-package-repository-preferred---opensuse-423"></a><span data-ttu-id="e80ae-204">패키지 리포지토리를 통해 설치(권장) - OpenSUSE 42.3</span><span class="sxs-lookup"><span data-stu-id="e80ae-204">Installation via Package Repository (preferred) - OpenSUSE 42.3</span></span>

<span data-ttu-id="e80ae-205">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 공식 Microsoft 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-205">PowerShell Core for Linux is published to official Microsoft repositories for easy installation (and updates).</span></span>

```sh
# Register the Microsoft signature key
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

# Add the Microsoft Repository
zypper ar https://packages.microsoft.com/rhel/7/prod/

# Update the list of products
sudo zypper update

# Install PowerShell
sudo zypper install powershell

# Start PowerShell
pwsh
```

### <a name="installation-via-direct-download---opensuse-423"></a><span data-ttu-id="e80ae-206">직접 다운로드를 통해 설치 - OpenSUSE 42.3</span><span class="sxs-lookup"><span data-stu-id="e80ae-206">Installation via Direct Download - OpenSUSE 42.3</span></span>

<span data-ttu-id="e80ae-207">[릴리스][] 페이지의 RPM 패키지 `powershell-6.0.2-1.rhel.7.x86_64.rpm`을 OpenSUSE 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-207">Download the RPM package `powershell-6.0.2-1.rhel.7.x86_64.rpm` from the [releases][] page onto the OpenSUSE machine.</span></span>

```sh
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo zypper install powershell-6.0.2-1.rhel.7.x86_64.rpm
```

<span data-ttu-id="e80ae-208">또한 다운로드의 중간 단계 없이 RPM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-208">You can also install the RPM without the intermediate step of downloading it:</span></span>

```sh
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo zypper install https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-1.rhel.7.x86_64.rpm
```

### <a name="uninstallation---opensuse-423"></a><span data-ttu-id="e80ae-209">제거 - OpenSUSE 42.3</span><span class="sxs-lookup"><span data-stu-id="e80ae-209">Uninstallation - OpenSUSE 42.3</span></span>

```sh
sudo zypper remove powershell
```

## <a name="fedora"></a><span data-ttu-id="e80ae-210">Fedora</span><span class="sxs-lookup"><span data-stu-id="e80ae-210">Fedora</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-211">Fedora 28은 PowerShell Core 6.1 이상에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-211">Fedora 28 is only supported in PowerShell Core 6.1 and newer.</span></span>

### <a name="installation-via-package-repository-preferred---fedora-27-fedora-28"></a><span data-ttu-id="e80ae-212">패키지 리포지토리를 통해 설치(권장) - Fedora 27, Fedora 28</span><span class="sxs-lookup"><span data-stu-id="e80ae-212">Installation via Package Repository (preferred) - Fedora 27, Fedora 28</span></span>

<span data-ttu-id="e80ae-213">PowerShell Core for Linux는 간편한 설치(및 업데이트)를 위해 공식 Microsoft 리포지토리로 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-213">PowerShell Core for Linux is published to official Microsoft repositories for easy installation (and updates).</span></span>

```sh
# Register the Microsoft signature key
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

# Register the Microsoft RedHat repository
curl https://packages.microsoft.com/config/rhel/7/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo

# Update the list of products
sudo dnf update

# Install a system component
sudo dnf install compat-openssl10

# Install PowerShell
sudo dnf install -y powershell

# Start PowerShell
pwsh
```

### <a name="installation-via-direct-download---fedora-27-fedora-28"></a><span data-ttu-id="e80ae-214">직접 다운로드를 통해 설치 - Fedora 27, Fedora 28</span><span class="sxs-lookup"><span data-stu-id="e80ae-214">Installation via Direct Download - Fedora 27, Fedora 28</span></span>

<span data-ttu-id="e80ae-215">[릴리스][] 페이지의 RPM 패키지 `powershell-6.0.2-1.rhel.7.x86_64.rpm`을 Fedora 컴퓨터에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-215">Download the RPM package `powershell-6.0.2-1.rhel.7.x86_64.rpm` from the [releases][] page onto the Fedora machine.</span></span>

<span data-ttu-id="e80ae-216">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-216">Then execute the following in the terminal:</span></span>

```sh
sudo dnf install compat-openssl10
sudo dnf install powershell-6.0.2-1.rhel.7.x86_64.rpm
```

<span data-ttu-id="e80ae-217">또한 다운로드의 중간 단계 없이 RPM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-217">You can also install the RPM without the intermediate step of downloading it:</span></span>

```sh
sudo dnf install compat-openssl10
sudo dnf install https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-1.rhel.7.x86_64.rpm
```

### <a name="uninstallation---fedora-27-fedora-28"></a><span data-ttu-id="e80ae-218">제거 - Fedora 27, Fedora 28</span><span class="sxs-lookup"><span data-stu-id="e80ae-218">Uninstallation - Fedora 27, Fedora 28</span></span>

```sh
sudo dnf remove powershell
```

## <a name="arch-linux"></a><span data-ttu-id="e80ae-219">Arch Linux</span><span class="sxs-lookup"><span data-stu-id="e80ae-219">Arch Linux</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-220">Arch 지원은 실험적입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-220">Arch support is experimental.</span></span>

<span data-ttu-id="e80ae-221">PowerShell은 [Arch Linux][] 사용자 리포지토리(AUR)에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-221">PowerShell is available from the [Arch Linux][] User Repository (AUR).</span></span>

* <span data-ttu-id="e80ae-222">[최신 태깅 릴리스][arch-release]를 사용하여 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-222">It can be compiled with the [latest tagged release][arch-release]</span></span>
* <span data-ttu-id="e80ae-223">[최신 마스터 커밋][arch-git]에서 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-223">It can be compiled from the [latest commit to master][arch-git]</span></span>
* <span data-ttu-id="e80ae-224">[최신 릴리스 이진 파일][arch-bin]을 사용하여 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-224">It can be installed using the [latest release binary][arch-bin]</span></span>

<span data-ttu-id="e80ae-225">AUR의 패키지는 커뮤니티에서 유지 관리되며 공식적인 지원은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-225">Packages in the AUR are community maintained - there is no official support.</span></span>

<span data-ttu-id="e80ae-226">AUR에서 패키지를 설치하는 방법에 대한 자세한 내용은 [Arch Linux wiki](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages) 또는 [DockerFile](https://github.com/PowerShell/PowerShell/blob/master/docker/community/archlinux/Dockerfile) 커뮤니티를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e80ae-226">For more information on installing packages from the AUR, see the [Arch Linux wiki](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages) or the community [DockerFile](https://github.com/PowerShell/PowerShell/blob/master/docker/community/archlinux/Dockerfile).</span></span>

[Arch Linux]: https://www.archlinux.org/download/
[arch-release]: https://aur.archlinux.org/packages/powershell/
[arch-git]: https://aur.archlinux.org/packages/powershell-git/
[arch-bin]: https://aur.archlinux.org/packages/powershell-bin/

## <a name="snap-package"></a><span data-ttu-id="e80ae-228">맞춤 패키지</span><span class="sxs-lookup"><span data-stu-id="e80ae-228">Snap Package</span></span>

### <a name="getting-snapd"></a><span data-ttu-id="e80ae-229">snapd 가져오기</span><span class="sxs-lookup"><span data-stu-id="e80ae-229">Getting snapd</span></span>

<span data-ttu-id="e80ae-230">`snapd`는 맞춤을 실행하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-230">`snapd` is required to run snaps.</span></span>  <span data-ttu-id="e80ae-231">[이러한 지침](https://docs.snapcraft.io/core/install)을 사용하여 `snapd`를 설치했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-231">Use [these instructions](https://docs.snapcraft.io/core/install) to make sure you have `snapd` installed.</span></span>

### <a name="installation-via-snap"></a><span data-ttu-id="e80ae-232">맞춤을 통해 설치</span><span class="sxs-lookup"><span data-stu-id="e80ae-232">Installation via Snap</span></span>

<span data-ttu-id="e80ae-233">Linux용 PowerShell Core는 간편한 설치 및 업데이트를 위해 [맞춤 저장소](https://snapcraft.io/store)에 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-233">PowerShell Core, for Linux, is published to the [Snap store](https://snapcraft.io/store) for easy installation (and updates).</span></span>
<span data-ttu-id="e80ae-234">기본 설정 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-234">This is the preferred method.</span></span>

```sh
# Install PowerShell
sudo snap install powershell-preview --classic

# Start PowerShell
pwsh-preview
```

<span data-ttu-id="e80ae-235">맞춤 설치를 자동으로 업그레이드한 후에 `sudo snap refresh powershell-preview`를 사용하여 업그레이드를 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-235">After installing Snap will automatically upgrade, but you can trigger an upgrade using `sudo snap refresh powershell-preview`.</span></span>

### <a name="uninstallation"></a><span data-ttu-id="e80ae-236">제거</span><span class="sxs-lookup"><span data-stu-id="e80ae-236">Uninstallation</span></span>

```sh
sudo snap remove powershell-preview
```

## <a name="linux-appimage"></a><span data-ttu-id="e80ae-237">Linux AppImage</span><span class="sxs-lookup"><span data-stu-id="e80ae-237">Linux AppImage</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-238">AppImage 지원은 실험적입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-238">AppImage support is experimental</span></span>

<span data-ttu-id="e80ae-239">최신 Linux 배포를 사용하여 [릴리스][] 페이지의 AppImage `powershell-6.0.1-x86_64.AppImage`를 Linux 컴퓨터로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-239">Using a recent Linux distribution, download the AppImage `powershell-6.0.1-x86_64.AppImage` from the [releases][] page onto the Linux machine.</span></span>

<span data-ttu-id="e80ae-240">그런 다음 터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-240">Then execute the following in the terminal:</span></span>

```bash
chmod a+x powershell-6.0.1-x86_64.AppImage
./powershell-6.0.1-x86_64.AppImage
```

<span data-ttu-id="e80ae-241">[AppImage][]를 사용하면 PowerShell을 설치하지 않고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-241">The [AppImage][] lets you run PowerShell without installing it.</span></span>
<span data-ttu-id="e80ae-242">PowerShell 및 종속성(.NET Core의 시스템 종속성 포함)을 하나의 통합 패키지로 묶은 이식 가능한 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-242">It is a portable application that bundles PowerShell and its dependencies (including .NET Core's system dependencies) into one cohesive package.</span></span>
<span data-ttu-id="e80ae-243">이 패키지는 사용자의 Linux 배포와 독립적으로 작동하는 단일 이진 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-243">This package is a single binary that works independently of the user's Linux distribution.</span></span>

[appimage]: http://appimage.org/

## <a name="kali"></a><span data-ttu-id="e80ae-245">Kali</span><span class="sxs-lookup"><span data-stu-id="e80ae-245">Kali</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-246">Kali 지원은 실험적입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-246">Kali support is experimental.</span></span>

### <a name="installation"></a><span data-ttu-id="e80ae-247">설치</span><span class="sxs-lookup"><span data-stu-id="e80ae-247">Installation</span></span>

```sh
# Download & Install prerequisites
sudo apt-get install libunwind8 libicu55
wget http://security.debian.org/debian-security/pool/updates/main/o/openssl/libssl1.0.0_1.0.1t-1+deb8u6_amd64.deb
sudo dpkg -i libssl1.0.0_1.0.1t-1+deb8u6_amd64.deb

# Install PowerShell
sudo dpkg -i powershell_6.0.2-1.ubuntu.16.04_amd64.deb

# Start PowerShell
pwsh
```

### <a name="run-powershell-in-latest-kali-kali-gnulinux-rolling-without-installing-it"></a><span data-ttu-id="e80ae-248">PowerShell을 설치하지 않고 최신 Kali(Kali GNU/Linux 롤링)에서 실행</span><span class="sxs-lookup"><span data-stu-id="e80ae-248">Run PowerShell in latest Kali (Kali GNU/Linux Rolling) without installing it</span></span>

```sh
# Grab the latest App Image
wget https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-x86_64.AppImage

# Make executable
chmod a+x powershell-6.0.2-x86_64.AppImage

# Start PowerShell
./powershell-6.0.2-x86_64.AppImage
```

### <a name="uninstallation---kali"></a><span data-ttu-id="e80ae-249">제거 - Kali</span><span class="sxs-lookup"><span data-stu-id="e80ae-249">Uninstallation - Kali</span></span>

```sh
sudo dpkg -r powershell_6.0.2-1.ubuntu.16.04_amd64.deb
```

## <a name="raspbian"></a><span data-ttu-id="e80ae-250">Raspbian</span><span class="sxs-lookup"><span data-stu-id="e80ae-250">Raspbian</span></span>

> [!NOTE]
> <span data-ttu-id="e80ae-251">Raspbian 지원은 실험적입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-251">Raspbian support is experimental.</span></span>

<span data-ttu-id="e80ae-252">현재 PowerShell은 Raspbian Stretch에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-252">Currently, PowerShell is only supported on Raspbian Stretch.</span></span>

<span data-ttu-id="e80ae-253">또한 [Pi Zero](https://github.com/dotnet/coreclr/issues/10605) 등의 다른 장치에는 지원되지 않는 프로세서가 있기 때문에 CoreCLR(및 PowerShell Core)은 Pi 2 및 Pi 3 장치에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-253">Also CoreCLR (and thus PowerShell Core) will only work on Pi 2 and Pi 3 devices as other devices, like [Pi Zero](https://github.com/dotnet/coreclr/issues/10605), have an unsupported processor.</span></span>

<span data-ttu-id="e80ae-254">[Raspbian Stretch](https://www.raspberrypi.org/downloads/raspbian/)를 다운로드하고 [설치 지침](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)에 따라 Pi에 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-254">Download [Raspbian Stretch](https://www.raspberrypi.org/downloads/raspbian/) and follow the [installation instructions](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) to get it onto your Pi.</span></span>

### <a name="installation"></a><span data-ttu-id="e80ae-255">설치</span><span class="sxs-lookup"><span data-stu-id="e80ae-255">Installation</span></span>

```sh
# Install prerequisites
sudo apt-get install libunwind8

# Grab the latest tar.gz
wget https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-linux-arm32.tar.gz

# Make folder to put powershell
mkdir ~/powershell

# Unpack the tar.gz file
tar -xvf ./powershell-6.0.2-linux-arm32.tar.gz -C ~/powershell

# Start PowerShell
~/powershell/pwsh
```

<span data-ttu-id="e80ae-256">필요에 따라 심볼 링크를 만들어 “pwsh” 이진 파일의 경로를 지정하지 않고 PowerShell을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-256">Optionally you can create a symbolic link to be able to start PowerShell without specifying path to the "pwsh" binary</span></span>

```sh
# Start PowerShell from bash with sudo to create a symbolic link
sudo ~/powershell/pwsh -c New-Item -ItemType SymbolicLink -Path "/usr/bin/pwsh" -Target "\$PSHOME/pwsh" -Force

# alternatively you can run following to create a symbolic link
# sudo ln -s ~/powershell/pwsh /usr/bin/pwsh

# Now to start PowerShell you can just run "pwsh"
```

### <a name="uninstallation---raspbian"></a><span data-ttu-id="e80ae-257">제거 - Raspbian</span><span class="sxs-lookup"><span data-stu-id="e80ae-257">Uninstallation - Raspbian</span></span>

```sh
rm -rf ~/powershell
```

## <a name="binary-archives"></a><span data-ttu-id="e80ae-258">이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="e80ae-258">Binary Archives</span></span>

<span data-ttu-id="e80ae-259">고급 배포 시나리오를 지원하기 위해 Linux 플랫폼을 위한 PowerShell 이진 `tar.gz` 보관이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-259">PowerShell binary `tar.gz` archives are provided for Linux platforms to enable advanced deployment scenarios.</span></span>

### <a name="dependencies"></a><span data-ttu-id="e80ae-260">종속성</span><span class="sxs-lookup"><span data-stu-id="e80ae-260">Dependencies</span></span>

<span data-ttu-id="e80ae-261">PowerShell은 모든 Linux 배포를 위한 이식 가능한 이진 파일을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-261">PowerShell builds portable binaries for all Linux distributions.</span></span>
<span data-ttu-id="e80ae-262">하지만 .NET Core 런타임의 경우 다양한 배포판에 대한 여러 종속성이 필요하므로 PowerShell가 동일한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-262">But .NET Core runtime requires different dependencies on different distributions, and hence PowerShell does the same.</span></span>

<span data-ttu-id="e80ae-263">다음 차트는 여러 Linux 배포에서 공식적으로 지원되는 .NET Core 2.0 종속성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-263">The following chart shows the .NET Core 2.0 dependencies that are officially supported on different Linux distributions.</span></span>

| <span data-ttu-id="e80ae-264">OS</span><span class="sxs-lookup"><span data-stu-id="e80ae-264">OS</span></span>                 | <span data-ttu-id="e80ae-265">종속성</span><span class="sxs-lookup"><span data-stu-id="e80ae-265">Dependencies</span></span> |
| ------------------ | ------------ |
| <span data-ttu-id="e80ae-266">Ubuntu 14.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-266">Ubuntu 14.04</span></span>       | <span data-ttu-id="e80ae-267">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-267">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-268">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu52</span><span class="sxs-lookup"><span data-stu-id="e80ae-268">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu52</span></span> |
| <span data-ttu-id="e80ae-269">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-269">Ubuntu 16.04</span></span>       | <span data-ttu-id="e80ae-270">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-270">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-271">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu55</span><span class="sxs-lookup"><span data-stu-id="e80ae-271">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu55</span></span> |
| <span data-ttu-id="e80ae-272">Ubuntu 17.10</span><span class="sxs-lookup"><span data-stu-id="e80ae-272">Ubuntu 17.10</span></span>       | <span data-ttu-id="e80ae-273">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-273">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-274">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu57</span><span class="sxs-lookup"><span data-stu-id="e80ae-274">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu57</span></span> |
| <span data-ttu-id="e80ae-275">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="e80ae-275">Ubuntu 18.04</span></span>       | <span data-ttu-id="e80ae-276">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-276">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-277">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu60</span><span class="sxs-lookup"><span data-stu-id="e80ae-277">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu60</span></span> |
| <span data-ttu-id="e80ae-278">Debian 8(Jessie)</span><span class="sxs-lookup"><span data-stu-id="e80ae-278">Debian 8 (Jessie)</span></span>  | <span data-ttu-id="e80ae-279">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-279">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-280">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu52</span><span class="sxs-lookup"><span data-stu-id="e80ae-280">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.0, libicu52</span></span> |
| <span data-ttu-id="e80ae-281">Debian 9(Stretch)</span><span class="sxs-lookup"><span data-stu-id="e80ae-281">Debian 9 (Stretch)</span></span> | <span data-ttu-id="e80ae-282">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span><span class="sxs-lookup"><span data-stu-id="e80ae-282">libc6, libgcc1, libgssapi-krb5-2, liblttng-ust0, libstdc++6,</span></span> <br> <span data-ttu-id="e80ae-283">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.2, libicu57</span><span class="sxs-lookup"><span data-stu-id="e80ae-283">libcurl3, libunwind8, libuuid1, zlib1g, libssl1.0.2, libicu57</span></span> |
| <span data-ttu-id="e80ae-284">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-284">CentOS 7</span></span> <br> <span data-ttu-id="e80ae-285">Oracle Linux 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-285">Oracle Linux 7</span></span> <br> <span data-ttu-id="e80ae-286">RHEL 7</span><span class="sxs-lookup"><span data-stu-id="e80ae-286">RHEL 7</span></span> <br> <span data-ttu-id="e80ae-287">OpenSUSE OpenSUSE 42.3</span><span class="sxs-lookup"><span data-stu-id="e80ae-287">OpenSUSE OpenSUSE 42.3</span></span> | <span data-ttu-id="e80ae-288">libunwind, libcurl, openssl-libs, libicu</span><span class="sxs-lookup"><span data-stu-id="e80ae-288">libunwind, libcurl, openssl-libs, libicu</span></span> |
| <span data-ttu-id="e80ae-289">Fedora 27</span><span class="sxs-lookup"><span data-stu-id="e80ae-289">Fedora 27</span></span> <br> <span data-ttu-id="e80ae-290">Fedora 28</span><span class="sxs-lookup"><span data-stu-id="e80ae-290">Fedora 28</span></span> | <span data-ttu-id="e80ae-291">libunwind, libcurl, openssl-libs, libicu, compat-openssl10</span><span class="sxs-lookup"><span data-stu-id="e80ae-291">libunwind, libcurl, openssl-libs, libicu, compat-openssl10</span></span> |

<span data-ttu-id="e80ae-292">공식적으로 지원되지 않는 Linux 배포에 PowerShell 이진 파일을 배포하려면 별도의 단계를 통해 대상 OS에 필요한 종속성을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-292">To deploy PowerShell binaries on Linux distributions that are not officially supported, you need to install the necessary dependencies for the target OS in separate steps.</span></span>
<span data-ttu-id="e80ae-293">예를 들어 [Amazon Linux dockerfile][amazon-dockerfile]은 먼저 종속성을 설치한 후 Linux `tar.gz` 아카이브를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-293">For example, our [Amazon Linux dockerfile][amazon-dockerfile] installs dependencies first, and then extracts the Linux `tar.gz` archive.</span></span>

[amazon-dockerfile]: https://github.com/PowerShell/PowerShell/blob/master/docker/community/amazonlinux/Dockerfile

### <a name="installation---binary-archives"></a><span data-ttu-id="e80ae-294">설치 - 이진 아카이브</span><span class="sxs-lookup"><span data-stu-id="e80ae-294">Installation - Binary Archives</span></span>

#### <a name="linux"></a><span data-ttu-id="e80ae-295">Linux</span><span class="sxs-lookup"><span data-stu-id="e80ae-295">Linux</span></span>

```sh
# Download the powershell '.tar.gz' archive
curl -L -o /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v6.0.2/powershell-6.0.2-linux-x64.tar.gz

# Create the target folder where powershell will be placed
sudo mkdir -p /opt/microsoft/powershell/6.0.2

# Expand powershell to the target folder
sudo tar zxf /tmp/powershell.tar.gz -C /opt/microsoft/powershell/6.0.2

# Set execute permissions
sudo chmod +x /opt/microsoft/powershell/6.0.2/pwsh

# Create the symbolic link that points to pwsh
sudo ln -s /opt/microsoft/powershell/6.0.2/pwsh /usr/bin/pwsh
```

### <a name="uninstalling-binary-archives"></a><span data-ttu-id="e80ae-296">이진 보관 제거</span><span class="sxs-lookup"><span data-stu-id="e80ae-296">Uninstalling binary archives</span></span>

```sh
sudo rm -rf /usr/bin/pwsh /opt/microsoft/powershell
```

## <a name="paths"></a><span data-ttu-id="e80ae-297">경로</span><span class="sxs-lookup"><span data-stu-id="e80ae-297">Paths</span></span>

* <span data-ttu-id="e80ae-298">`$PSHOME`은 `/opt/microsoft/powershell/6.0.2/`입니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-298">`$PSHOME` is `/opt/microsoft/powershell/6.0.2/`</span></span>
* <span data-ttu-id="e80ae-299">사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-299">User profiles will be read from `~/.config/powershell/profile.ps1`</span></span>
* <span data-ttu-id="e80ae-300">기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-300">Default profiles will be read from `$PSHOME/profile.ps1`</span></span>
* <span data-ttu-id="e80ae-301">사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-301">User modules will be read from `~/.local/share/powershell/Modules`</span></span>
* <span data-ttu-id="e80ae-302">공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-302">Shared modules will be read from `/usr/local/share/powershell/Modules`</span></span>
* <span data-ttu-id="e80ae-303">기본 모듈은 `$PSHOME/Modules`에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-303">Default modules will be read from `$PSHOME/Modules`</span></span>
* <span data-ttu-id="e80ae-304">PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-304">PSReadline history will be recorded to `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`</span></span>

<span data-ttu-id="e80ae-305">프로필은 PowerShell의 호스트별 구성을 계속 사용하므로 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-305">The profiles respect PowerShell's per-host configuration, so the default host-specific profiles exists at `Microsoft.PowerShell_profile.ps1` in the same locations.</span></span>

<span data-ttu-id="e80ae-306">PowerShell은 Linux의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="e80ae-306">PowerShell respects the [XDG Base Directory Specification][xdg-bds] on Linux.</span></span>

[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[releases]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
