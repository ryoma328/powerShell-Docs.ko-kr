---
ms.date: 06/12/2017
keywords: dsc,powershell,configuration,setup
title: Linux용 DSC nxGroup 리소스
ms.openlocfilehash: c61b6ab4a8c56d085b5297dcfc7582187d54f946
ms.sourcegitcommit: 77f62a55cac8c13d69d51eef5fade18f71d66955
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/17/2018
ms.locfileid: "39093605"
---
# <a name="dsc-for-linux-nxgroup-resource"></a>Linux용 DSC nxGroup 리소스

PowerShell DSC(필요한 상태 구성)의 **nxGroup** 리소스에서는 Linux 노드에 있는 로컬 그룹을 관리하는 메커니즘을 제공합니다.

## <a name="syntax"></a>구문

```
nxGroup <string> #ResourceName
{
    GroupName = <string>
    [ Ensure = <string> { Absent | Present } ]
    [ Members = <string[]> ]
    [ MembersToInclude = <string[]> ]
    [ MembersToExclude = <string[]> ]
    [ DependsOn = <string[]> ]
}
```

## <a name="properties"></a>속성

|  속성 |  설명 |
|---|---|
| GroupName| 특정 상태를 확인하려는 그룹의 이름을 지정합니다.|
| Ensure| 해당 그룹이 존재하는지를 확인할지 여부를 결정합니다. 해당 그룹이 존재하도록 하려면 이 속성을 "Present"으로 설정합니다. 해당 그룹이 존재하지 않도록 하려면 이 속성을 "Absent"으로 설정합니다. 기본값은 "Present"입니다.|
| 구성원| 그룹을 형성하는 구성원을 지정합니다.|
| MembersToInclude| 이 그룹의 구성원이 되도록 할 사용자를 지정합니다.|
| MembersToExclude| 이 그룹의 구성원이 되지 않도록 할 사용자를 지정합니다.|
| PreferredGroupID| 가능한 경우 그룹 ID를 제공된 값으로 설정합니다. 현재 그룹 ID가 사용 중이라면 다음의 사용 가능한 그룹 ID가 사용됩니다.|
| DependsOn | 이 리소스를 구성하려면 먼저 다른 리소스의 구성을 실행해야 함을 나타냅니다. 예를 들어, 먼저 실행하려는 리소스 구성 스크립트 블록의 **ID**가 **ResourceName**이고 해당 형식이 **ResourceType**일 경우, 이 속성을 사용하기 위한 구문은 `DependsOn = '[ResourceType]ResourceName'`입니다.|

## <a name="example"></a>예제

다음 예제에서는 사용자 ‘monuser’가 존재하고 ‘DBusers’ 그룹의 구성원임을 확인합니다.

```powershell
Import-DSCResource -Module nx

Node $node {
    nxUser UserExample {
       UserName = 'monuser'
       Description = 'Monitoring user'
       Password = '$6$fZAne/Qc$MZejMrOxDK0ogv9SLiBP5J5qZFBvXLnDu8HY1Oy7ycX.Y3C7mGPUfeQy3A82ev3zIabhDQnj2ayeuGn02CqE/0'
       Ensure = 'Present'
       HomeDirectory = '/home/monuser'
    }

    nxGroup GroupExample {
       GroupName = 'DBusers'
       Ensure = 'Present'
       MembersToInclude = 'monuser'
       DependsOn = '[nxUser]UserExample'
    }
}
```