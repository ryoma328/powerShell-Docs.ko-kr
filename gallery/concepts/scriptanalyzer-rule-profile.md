---
ms.date: 06/12/2017
contributor: JKeithB
keywords: gallery,powershell,cmdlet,psgallery
title: 갤러리에 대한 ScriptAnazlyer 규칙 프로필
ms.openlocfilehash: d91a88981cc2f3269a1f8b6ee864f8333a2f097c
ms.sourcegitcommit: 98b7cfd8ad5718efa8e320526ca76c3cc4141d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50002499"
---
# <a name="scriptanalyzer-rule-profile-for-gallery"></a>갤러리에 대한 ScriptAnazlyer 규칙 프로필

PowerShell 갤러리에 게시된 패키지의 품질을 보장하기 위해 [PSScriptAnalyzer](https://github.com/PowerShell/PSScriptAnalyzer) 규칙을 실행하여 제출된 스크립트에 위반 사항이 있는지 확인합니다.

ScriptAnalyzer [GitHub 페이지](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/Engine/Settings/PSGallery.psd1)에서 실행하는 규칙의 목록을 찾을 수 있습니다.
실행하는 규칙과 관련해서 질문이 있는 경우 PowerShell 갤러리 관리자에게 문의하거나 ScriptAnalzyer에 대한 문제를 개설합니다.

ScriptAnalyzer 결과는 향후 릴리스의 갤러리에 포함된 각 개별 패키지 페이지에 표시됩니다. 패키지 소유자는 해당 패키지를 확인하여 게시된 패키지에 심각한 오류가 없는지 검토하는 것이 좋습니다.
