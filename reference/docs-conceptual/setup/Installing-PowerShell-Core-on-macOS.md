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
# <a name="installing-powershell-core-on-macos"></a>macOS에서 PowerShell Core 설치

PowerShell Core는 macOS 10.12 이상을 지원합니다.
모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.
패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.

## <a name="installation-of-latest-stable-release-via-homebrew-on-macos-1012-or-higher"></a>macOS 10.12 이상에서 Homebrew를 통해 안정적인 최신 릴리스 설치

[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.
`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.

이제 PowerShell을 설치할 수 있습니다.

```sh
brew cask install powershell
```

최종적으로, 설치가 제대로 작동하는지 확인합니다.

```sh
pwsh
```

PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> 위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만, 업그레이드를 완료하기 위해 PowerShell 셸을 종료하고 다시 시작해야 합니다.
> $PSVersionTable에 표시된 값을 새로 고칩니다.

[brew]: http://brew.sh/

## <a name="installation-of-latest-preview-release-via-homebrew-on-macos-1012-or-higher"></a>macOS 10.12 이상에서 Homebrew를 통해 최신 미리 보기 릴리스 설치

[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.
`brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.

Homebrew를 설치했으면 PowerShell을 쉽게 설치할 수 있습니다.
먼저, Cask 패키지의 다른 버전을 설치할 수 있는 [Cask-버전][cask-versions]을 설치합니다.

```sh
brew tap homebrew/cask-versions
```

이제 PowerShell을 설치할 수 있습니다.

```sh
brew cask install powershell-preview
```

최종적으로, 설치가 제대로 작동하는지 확인합니다.

```sh
pwsh-preview
```

PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> 위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만, 업그레이드를 완료하기 위해 PowerShell 셸을 종료하고 다시 시작해야 합니다.
> $PSVersionTable에 표시된 값을 새로 고칩니다.

## <a name="installation-via-direct-download"></a>직접 다운로드를 통해 설치

PKG 패키지 `powershell-6.1.0-osx-x64.pkg`를
[릴리스][] 페이지에서 macOS 머신으로 다운로드합니다.

파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.

```sh
sudo installer -pkg powershell-6.1.0-osx-x64.pkg -target /
```

## <a name="binary-archives"></a>이진 아카이브

고급 배포 시나리오를 사용하도록 설정하려면 macOS 플랫폼에 대해 PowerShell 이진 `tar.gz` 보관이 제공됩니다.

### <a name="installing-binary-archives-on-macos"></a>macOS에서 이진 보관 설치

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

## <a name="uninstalling-powershell-core"></a>PowerShell Core 제거

Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.

```sh
brew cask uninstall powershell
```

직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

추가 PowerShell 경로를 제거하려면 이 문서의 [경로](#paths) 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.

> [!NOTE]
> Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.

## <a name="paths"></a>경로

* `$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`입니다.
* 사용자 프로필은 `~/.config/powershell/profile.ps1`에서 읽습니다.
* 기본 프로필은 `$PSHOME/profile.ps1`에서 읽습니다.
* 사용자 프로필은 `~/.local/share/powershell/Modules`에서 읽습니다.
* 공유 모듈은 `/usr/local/share/powershell/Modules`에서 읽습니다.
* 기본 모듈은 `$PSHOME/Modules`에서 읽습니다.
* PSReadline 기록은 `~/.local/share/powershell/PSReadLine/ConsoleHost_history.txt`에 기록됩니다.

프로필은 PowerShell의 호스트별 구성을 반영합니다.
따라서 기본 호스트별 프로필은 동일한 위치의 `Microsoft.PowerShell_profile.ps1`에 있습니다.

PowerShell은 macOS의 [XDG 기본 디렉터리 사양][xdg-bds]을 따릅니다.

macOS는 BSD에서 파생된 것이므로 `/opt` 대신 `/usr/local`이 접두사로 사용됩니다.
따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.1.0/`이며 symlink는 `/usr/local/bin/pwsh`에 있습니다.

## <a name="additional-resources"></a>추가 리소스

* [Homebrew 웹][brew]
* [Homebrew Github 리포지토리][GitHub]
* [Homebrew-Cask][cask]

[brew]: http://brew.sh/
[Cask]: https://github.com/Homebrew/homebrew-cask
[cask-versions]: https://github.com/Homebrew/homebrew-cask-versions
[GitHub]: https://github.com/Homebrew
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
