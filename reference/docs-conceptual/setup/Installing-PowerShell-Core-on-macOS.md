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
# <a name="installing-powershell-core-on-macos"></a>macOS에서 PowerShell Core 설치

PowerShell Core는 macOS 10.12 이상을 지원합니다.
모든 패키지는 GitHub [릴리스][] 페이지에 제공됩니다.
패키지가 설치되면 터미널에서 `pwsh`를 실행합니다.

### <a name="installation-via-homebrew-on-macos-1012"></a>macOS 10.12 이상에서 Homebrew를 통해 설치

[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.
터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.  `brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.

> [!NOTE]
> 이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.
```sh
brew update-reset
brew update
```

> Homebrew의 이전 버전에서는 ‘caskroom/cask’를 사용했으나, 더 이상 사용되지 않고 ‘homebrew/cask’로 마이그레이션되었습니다.  자세한 내용은 [Homebrew-cask][cask]를 참조하세요. ‘brew tap’ 명령을 사용하여 현재 탭을 나열합니다.  ‘caskroom/cask’가 표시되면 ‘brew update’를 사용하여 Homebrew가 탭을 마이그레이션하게 할 수 있습니다.

```sh
brew tap
brew update
```

Homebrew를 설치/업데이트한 후 PowerShell을 쉽게 설치할 수 있습니다.

PowerShell을 설치하려면

```sh
brew cask install powershell
```

최종적으로, 설치가 제대로 작동하는지 확인합니다.

```sh
pwsh
```

PowerShell을 종료하고 bash로 돌아가려면 ‘exit’ 명령을 사용합니다.
```sh
exit
```

PowerShell의 새 버전이 릴리스되면 Homebrew의 공식을 업데이트하고 PowerShell을 업그레이드하기만 하면 됩니다.

```sh
brew update
brew cask upgrade powershell
```

> [!NOTE]
> 위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.

### <a name="installing-preview-via-homebrew-on-macos-1012"></a>macOS 10.12 이상에서 Homebrew를 통해 미리 보기 설치

[Homebrew][brew]는 macOS용 기본 패키지 관리자입니다.
터미널 창에서 `brew`를 입력하여 Homebrew를 실행합니다.  `brew` 명령이 없을 경우 [해당 지침][brew]에 따라 Homebrew를 설치해야 합니다.

> [!NOTE]
> 이전에 Homebrew를 설치한 경우 항상 'brew update-reset' 및 'brew update'를 실행하는 것이 좋습니다.
```sh
brew update-reset
brew update
```

그런 다음, 미리 보기 패키지를 가져오려면 `versions` casks 리포지토리를 탭해야 합니다.

```sh
brew tap homebrew/cask-versions
```

PowerShell 미리 보기를 설치하려면:

```sh
brew cask install powershell-preview
```

최종적으로, 설치가 제대로 작동하는지 확인합니다.

```sh
pwsh-preview
```

PowerShell의 새 버전이 릴리스되면 Homebrew의 수식을 업데이트하고 PowerShell 미리 보기를 업그레이드하면 됩니다.

```sh
brew update
brew cask upgrade powershell-preview
```

> [!NOTE]
> 위의 명령은 PowerShell(pwsh) 호스트 내에서 호출할 수 있지만 이때 PowerShell 셸을 종료하고 다시 시작하여 업그레이드를 완료하고 $PSVersionTable에 표시된 값을 새로 고쳐야 합니다.

### <a name="installation-via-direct-download"></a>직접 다운로드를 통해 설치

[릴리스][] 페이지의 PKG 패키지 `powershell-6.0.2-osx.10.12-x64.pkg`를 macOS 컴퓨터로 다운로드합니다.

파일을 두 번 클릭하고 메시지를 따르거나 터미널에서 설치할 수 있습니다.

```sh
sudo installer -pkg powershell-6.0.2-osx.10.12-x64.pkg -target /
```

## <a name="binary-archives"></a>이진 아카이브

고급 배포 시나리오를 지원하기 위해 macOS 및 Linux 플랫폼에 PowerShell 이진 `tar.gz` 아카이브가 제공됩니다.

### <a name="installing-binary-archives-on-macos"></a>macOS에서 이진 보관 설치

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

## <a name="uninstalling-powershell-core"></a>PowerShell Core 제거

Homebrew를 사용하여 PowerShell을 설치한 경우에는 제거가 간편합니다.

```sh
brew cask uninstall powershell
```

직접 다운로드를 통해 PowerShell을 설치한 경우에는 PowerShell을 수동으로 제거해야 합니다.

```sh
sudo rm -rf /usr/local/bin/pwsh /usr/local/microsoft/powershell
```

추가 PowerShell 경로를 제거하려면 이 문서의 [경로][] 섹션을 참조하고 `sudo rm`을 사용하여 원하는 경로를 제거합니다.

> [!NOTE]
> Homebrew를 사용하여 설치한 경우에는 필요하지 않습니다.

[경로]:#paths

## <a name="paths"></a>경로

* `$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`입니다.
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
따라서 `$PSHOME`은 `/usr/local/microsoft/powershell/6.0.2/`이며 symlink는 `/usr/local/bin/pwsh`에 있습니다.

## <a name="additional-resources"></a>추가 리소스

* [Homebrew 웹][brew]
* [Homebrew Github 리포지토리][GitHub]
* [Homebrew-Cask][cask]


[brew]: http://brew.sh/
[GitHub]: https://github.com/Homebrew
[Cask]: https://github.com/Homebrew/homebrew-cask
[릴리스]: https://github.com/PowerShell/PowerShell/releases/latest
[xdg-bds]: https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html
