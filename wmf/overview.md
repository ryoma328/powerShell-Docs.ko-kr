---
ms.date: 06/12/2018
keywords: wmf,powershell,setup
title: WMF(Windows Management Framework)
ms.openlocfilehash: 17011f88c364cb56a0c87f092873ccd99db450bc
ms.sourcegitcommit: 68093cc12a7a22c53d11ce7d33c18622921a0dd1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2018
ms.locfileid: "36943613"
---
# <a name="windows-management-framework"></a>Windows Management Framework

WMF(Windows Management Framework)는 Windows에 대한 일관적인 관리 인터페이스를 제공합니다. WMF는 다양한 버전의 Windows 클라이언트 및 Windows Server를 관리하는 원활한 방법을 제공합니다. WMF 설치 관리자 패키지는 관리 기능에 대한 업데이트를 포함하고 이전 버전의 Windows에 대해 지원됩니다.

WMF 설치는 다음 기능을 추가 및/또는 업데이트합니다.

- Windows PowerShell
- Windows PowerShell DSC(원하는 상태 구성)
- Windows PowerShell ISE(통합 스크립트 환경)
- WinRM(Windows Remote Management)
- WMI(Windows Management Instrumentation)
- Windows PowerShell 웹 서비스(관리 OData IIS 확장)
- 소프트웨어 인벤토리 로깅(SIL)
- 서버 관리자 CIM 공급자

## <a name="wmf-release-notes"></a>WMF 릴리스 정보

PowerShell 및 지정된 WMF의 다른 구성 요소에서 향상된 다양한 기능에 대해 알아보려면 아래 링크에서 릴리스 정보를 참조하세요.

- [WMF 5.1](5.1/release-notes.md)
- [WMF 5.0](5.0/releasenotes.md)
- [WMF 4.0](https://download.microsoft.com/download/3/D/6/3D61D262-8549-4769-A660-230B67E15B25/Windows%20Management%20Framework%204%200%20Release%20Notes.docx)
- [WMF 3.0](https://download.microsoft.com/download/E/7/6/E76850B8-DA6E-4FF5-8CCE-A24FC513FD16/WMF%203%20Release%20Notes.docx)

## <a name="wmf-availability-across-windows-operating-systems"></a>Windows 운영 체제에서의 WMF 가용성

|운영 체제 버전  |[WMF 5.1][] |[WMF 5.0][] |[WMF 4.0][] |[WMF 3.0][]  |[WMF 2.0][] |
|--------------------------|------------|------------|------------|-------------|------------|
|Windows Server 2016       |함께 제공|            |            |             |            |
|Windows 10                |함께 제공|함께 제공|            |             |            |
|Windows Server 2012 R2    |예         |예         |함께 제공|             |            |
|Windows 8.1               |예         |예         |함께 제공|             |            |
|Windows Server 2012       |예         |예         |예         |함께 제공 |            |
|Windows 8                 |            |            |            |함께 제공 |            |
|Windows Server 2008 R2 SP1|예         |예         |예         |예          |함께 제공|
|Windows 7 SP1             |예         |예         |예         |예          |함께 제공|
|Windows Server 2008 SP2   |            |            |            |예          |예         |
|Windows Vista             |            |            |            |             |예         |
|Windows Server 2003       |            |            |            |             |예         |
|Windows XP                |            |            |            |예          |            |

**함께 제공**: 지정된 버전의 WMF 기능은 표시된 버전의 Windows 클라이언트 및 Windows Server에 제공되었습니다.

[WMF 5.1]: https://aka.ms/wmf51download
[WMF 5.0]: https://aka.ms/wmf5download
[WMF 4.0]: https://aka.ms/wmf4download
[WMF 3.0]: https://aka.ms/wmf3download
[WMF 2.0]: https://aka.ms/wmf2download
