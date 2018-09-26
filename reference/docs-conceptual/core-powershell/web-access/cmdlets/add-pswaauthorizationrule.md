---
ms.topic: reference
keywords: powershell,cmdlet
ms.date: 12/12/2016
title: Add-PswaAuthorizationRule
schema: 2.0.0
ms.openlocfilehash: fe2b71dcfa870ba3f92484ae3fd3c45b3107a1bc
ms.sourcegitcommit: e46b868f56f359909ff7c8230b1d1770935cce0e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45523082"
---
# <a name="add-pswaauthorizationrule"></a><span data-ttu-id="936e1-103">Add-PswaAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="936e1-103">Add-PswaAuthorizationRule</span></span>

## <a name="synopsis"></a><span data-ttu-id="936e1-104">요약</span><span class="sxs-lookup"><span data-stu-id="936e1-104">SYNOPSIS</span></span>

<span data-ttu-id="936e1-105">새로운 권한 부여 규칙을 Windows PowerShell 웹 액세스 권한 부여 규칙 집합에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-105">Adds a new authorization rule to the Windows PowerShell Web Access authorization rule set.</span></span>

## <a name="syntax"></a><span data-ttu-id="936e1-106">구문</span><span class="sxs-lookup"><span data-stu-id="936e1-106">Syntax</span></span>

### <a name="usergroupnamecomputergroupname"></a><span data-ttu-id="936e1-107">UserGroupNameComputerGroupName</span><span class="sxs-lookup"><span data-stu-id="936e1-107">UserGroupNameComputerGroupName</span></span>

```
Add-PswaAuthorizationRule -ComputerGroupName <String> -ConfigurationName <String> -UserGroupName <String[]> [-Credential <PSCredential> ] [-Force] [-RuleName <String> ] [ <CommonParameters>]
```

### <a name="usergroupnamecomputername"></a><span data-ttu-id="936e1-108">UserGroupNameComputerName</span><span class="sxs-lookup"><span data-stu-id="936e1-108">UserGroupNameComputerName</span></span>

```
Add-PswaAuthorizationRule -ComputerName <String> -ConfigurationName <String> -UserGroupName <String[]> [-Credential <PSCredential> ] [-Force] [-RuleName <String> ] [ <CommonParameters>]
```

### <a name="usernamecomputergroupname"></a><span data-ttu-id="936e1-109">UserNameComputerGroupName</span><span class="sxs-lookup"><span data-stu-id="936e1-109">UserNameComputerGroupName</span></span>

```
Add-PswaAuthorizationRule [-UserName] <String[]> -ComputerGroupName <String> -ConfigurationName <String> [-Credential <PSCredential> ] [-Force] [-RuleName <String> ] [ <CommonParameters>]
```

### <a name="usernamecomputername"></a><span data-ttu-id="936e1-110">UserNameComputerName</span><span class="sxs-lookup"><span data-stu-id="936e1-110">UserNameComputerName</span></span>

```
Add-PswaAuthorizationRule [-UserName] <String[]> [-ComputerName] <String> [-ConfigurationName] <String> [-Credential <PSCredential> ] [-Force] [-RuleName <String> ] [ <CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="936e1-111">설명</span><span class="sxs-lookup"><span data-stu-id="936e1-111">DESCRIPTION</span></span>

<span data-ttu-id="936e1-112">**Add-PswaAuthorizationRule** cmdlet은 새로운 권한 부여 규칙을 Windows PowerShell(r) 웹 액세스 권한 부여 규칙 집합에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-112">The **Add-PswaAuthorizationRule** cmdlet adds a new authorization rule to the Windows PowerShell(r) Web Access authorization rule set.</span></span>

<span data-ttu-id="936e1-113">이 규칙에 대한 사용자, 컴퓨터 및 Windows PowerShell 엔드포인트를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-113">You must specify the users, computers, and Windows PowerShell endpoints for this rule.</span></span> <span data-ttu-id="936e1-114">개별 사용자 및 컴퓨터 이름을 지정하거나 그룹을 지정하여 사용자 및 컴퓨터를 모두 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-114">You can specify both users and computers either by individual user accounts and computer names, or by specifying groups.</span></span>

<span data-ttu-id="936e1-115">Active Directory 도메인에 가입된 컴퓨터의 경우 이 cmdlet은 컴퓨터의 SID(보안 식별자)를 사용하여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-115">For a computer that is joined to an Active Directory domain, the cmdlet uses the security identifier (SID) of the computer to create the rule.</span></span> <span data-ttu-id="936e1-116">따라서 로그인 페이지의 **컴퓨터 이름** 필드에 약식 이름, FQDN(정규화된 도메인 이름 ) 또는 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-116">This allows you to use a short name, a fully qualified domain name (FQDN), or an IP address for the **Computer Name** field on the sign-in page.</span></span>

<span data-ttu-id="936e1-117">Active Directory 도메인에 가입되지 않은 컴퓨터의 경우 이 cmdlet은 관리자가 제공한 컴퓨터 이름을 사용하여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-117">For a computer that is not joined to an Active Directory domain, the cmdlet creates the rule using the computer name provided by the administrator.</span></span> <span data-ttu-id="936e1-118">이 컴퓨터에 연결하려면 최종 사용자는 컴퓨터 이름을 규칙에 표시된 대로 정확히 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-118">To successfully connect to this machine, the end user must provide the computer name exactly as it appears in the rule.</span></span>

<span data-ttu-id="936e1-119">네트워크에서 같은 이름의 컴퓨터가 여럿 있는 경우에는 약식 이름을 사용하여 둘 이상의 컴퓨터를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-119">If there are multiple computers with the same name on the network, then short name can resolve to more than one computer.</span></span> <span data-ttu-id="936e1-120">따라서 연결을 설정할 때 모호해질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-120">This can lead to ambiguity when establishing a connection.</span></span> <span data-ttu-id="936e1-121">예를 들어 “*Server1*”이라는 작업 그룹 컴퓨터에 대한 규칙이 있고 *server1.contoso.com*이라는 새 컴퓨터가 네트워크에 조인된 경우 권한 부여 규칙을 사용한 유효성 검사가 성공하고 Windows PowerShell 웹 액세스가 “*Server1*”이라는 컴퓨터에 대한 연결을 설정하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-121">For example, if a rule exists for the workgroup computer named "*Server1*" and a new computer named *server1.contoso.com* is joined to the network, validation using the authorization rules succeeds and Windows PowerShell Web Access attempts to establish a connection to the computer named "*Server1*".</span></span> <span data-ttu-id="936e1-122">지정된 작업 그룹 컴퓨터와의 연결이 설정된다는 보장은 없으며, 작업 그룹 또는 "*Server1*"이라는 도메인 컴퓨터에 대해 연결이 시도될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-122">It is not guaranteed that the connection is established with the specified workgroup computer; the attempt could be made on either the workgroup or the domain computer named "*Server1*".</span></span> <span data-ttu-id="936e1-123">모호성을 줄이기 위해 가능하면 대상 컴퓨터의 FQDN을 사용하여 권한 부여 규칙을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-123">To reduce ambiguity, it is recommended that you use the FQDN for the destination computer whenever possible to create an authorization rule.</span></span>

<span data-ttu-id="936e1-124">권한 부여 규칙에서는 대체 자격 증명(로그인 페이지의 **옵션 연결 설정** 섹션에 있는 두 번째 자격 증명 집합)이 아니라 Windows PowerShell 웹 액세스 사용자의 기본 로그인 자격 증명을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-124">The authorization rules evaluate the primary sign-in credential of the Windows PowerShell Web Access users, not the alternate credentials (the second set of credentials found in the **Optional connection settings** section of the sign-in page).</span></span> <span data-ttu-id="936e1-125">관련 예제는 예제 6을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="936e1-125">For an example of this, see Example 6.</span></span>

## <a name="parameters"></a><span data-ttu-id="936e1-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="936e1-126">Parameters</span></span>

### <a name="-computergroupname-string"></a><span data-ttu-id="936e1-127">-ComputerGroupName \<String\></span><span class="sxs-lookup"><span data-stu-id="936e1-127">-ComputerGroupName \<String\></span></span>

<span data-ttu-id="936e1-128">이 규칙이 액세스 권한을 부여하는 AD DS(Active Directory 도메인 서비스)의 컴퓨터 그룹 또는 로컬 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-128">Specifies the name of a computer group in Active Directory Domain Services (AD DS) or local groups to which this rule grants access.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-129">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-129">Aliases</span></span>                     | <span data-ttu-id="936e1-130">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-130">none</span></span>                  |
| <span data-ttu-id="936e1-131">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-131">Required?</span></span>                   | <span data-ttu-id="936e1-132">true</span><span class="sxs-lookup"><span data-stu-id="936e1-132">true</span></span>                  |
| <span data-ttu-id="936e1-133">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-133">Position?</span></span>                   | <span data-ttu-id="936e1-134">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-134">named</span></span>                 |
| <span data-ttu-id="936e1-135">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-135">Default Value</span></span>               | <span data-ttu-id="936e1-136">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-136">none</span></span>                  |
| <span data-ttu-id="936e1-137">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-137">Accept Pipeline Input?</span></span>      | <span data-ttu-id="936e1-138">True (ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-138">True (ByPropertyName)</span></span> |
| <span data-ttu-id="936e1-139">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-139">Accept Wildcard Characters?</span></span> | <span data-ttu-id="936e1-140">false</span><span class="sxs-lookup"><span data-stu-id="936e1-140">false</span></span>                 |

### <a name="-computername-string"></a><span data-ttu-id="936e1-141">-ComputerName \<String\></span><span class="sxs-lookup"><span data-stu-id="936e1-141">-ComputerName \<String\></span></span>

<span data-ttu-id="936e1-142">이 규칙이 액세스 권한을 부여하는 컴퓨터 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-142">Specifies the computer name to which this rule grants access.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-143">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-143">Aliases</span></span>                     | <span data-ttu-id="936e1-144">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-144">none</span></span>                  |
| <span data-ttu-id="936e1-145">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-145">Required?</span></span>                   | <span data-ttu-id="936e1-146">true</span><span class="sxs-lookup"><span data-stu-id="936e1-146">true</span></span>                  |
| <span data-ttu-id="936e1-147">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-147">Position?</span></span>                   | <span data-ttu-id="936e1-148">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-148">named</span></span>                 |
| <span data-ttu-id="936e1-149">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-149">Default Value</span></span>               | <span data-ttu-id="936e1-150">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-150">none</span></span>                  |
| <span data-ttu-id="936e1-151">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-151">Accept Pipeline Input?</span></span>      | <span data-ttu-id="936e1-152">True (ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-152">True (ByPropertyName)</span></span> |
| <span data-ttu-id="936e1-153">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-153">Accept Wildcard Characters?</span></span> | <span data-ttu-id="936e1-154">false</span><span class="sxs-lookup"><span data-stu-id="936e1-154">false</span></span>                 |

### <a name="-configurationname-string"></a><span data-ttu-id="936e1-155">-ConfigurationName \<String\></span><span class="sxs-lookup"><span data-stu-id="936e1-155">-ConfigurationName \<String\></span></span>

<span data-ttu-id="936e1-156">이 규칙이 액세스 권한을 부여하는 Windows PowerShell 세션 구성(runspace라고도 함)의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-156">Specifies the name of the Windows PowerShell session configuration, also known as runspace, to which this rule grants access.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-157">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-157">Aliases</span></span>                     | <span data-ttu-id="936e1-158">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-158">none</span></span>                  |
| <span data-ttu-id="936e1-159">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-159">Required?</span></span>                   | <span data-ttu-id="936e1-160">true</span><span class="sxs-lookup"><span data-stu-id="936e1-160">true</span></span>                  |
| <span data-ttu-id="936e1-161">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-161">Position?</span></span>                   | <span data-ttu-id="936e1-162">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-162">named</span></span>                 |
| <span data-ttu-id="936e1-163">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-163">Default Value</span></span>               | <span data-ttu-id="936e1-164">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-164">none</span></span>                  |
| <span data-ttu-id="936e1-165">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-165">Accept Pipeline Input?</span></span>      | <span data-ttu-id="936e1-166">True (ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-166">True (ByPropertyName)</span></span> |
| <span data-ttu-id="936e1-167">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-167">Accept Wildcard Characters?</span></span> | <span data-ttu-id="936e1-168">false</span><span class="sxs-lookup"><span data-stu-id="936e1-168">false</span></span>                 |

### <a name="-credential--pscredential"></a><span data-ttu-id="936e1-169">-Credential  \<PSCredential\></span><span class="sxs-lookup"><span data-stu-id="936e1-169">-Credential  \<PSCredential\></span></span>

<span data-ttu-id="936e1-170">Windows PowerShell 웹 액세스 권한 부여 규칙을 변경하는 데 사용할 사용자 계정에 대한 **PSCredential** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-170">Specifies a **PSCredential** object for a user account that you want to use to change Windows PowerShell Web Access authorization rules.</span></span> <span data-ttu-id="936e1-171">이 매개 변수를 추가하지 않으면 현재 로그온한 사용자 계정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-171">If you do not add this parameter, the cmdlet uses the currently logged-on user account.</span></span> <span data-ttu-id="936e1-172">권한 부여 규칙을 추가하는 데 필요한 **PSCredential**을 가져오려면 [Get-Credential](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.security/Get-Credential) cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-172">To get a **PSCredential** object, which is required to add authorization rules remotely, run the [Get-Credential](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.security/Get-Credential) cmdlet.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-173">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-173">Aliases</span></span>                     | <span data-ttu-id="936e1-174">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-174">none</span></span>  |
| <span data-ttu-id="936e1-175">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-175">Required?</span></span>                   | <span data-ttu-id="936e1-176">false</span><span class="sxs-lookup"><span data-stu-id="936e1-176">false</span></span> |
| <span data-ttu-id="936e1-177">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-177">Position?</span></span>                   | <span data-ttu-id="936e1-178">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-178">named</span></span> |
| <span data-ttu-id="936e1-179">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-179">Default Value</span></span>               | <span data-ttu-id="936e1-180">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-180">none</span></span>  |
| <span data-ttu-id="936e1-181">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-181">Accept Pipeline Input?</span></span>      | <span data-ttu-id="936e1-182">false</span><span class="sxs-lookup"><span data-stu-id="936e1-182">false</span></span> |
| <span data-ttu-id="936e1-183">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-183">Accept Wildcard Characters?</span></span> | <span data-ttu-id="936e1-184">false</span><span class="sxs-lookup"><span data-stu-id="936e1-184">false</span></span> |

### <a name="-force"></a><span data-ttu-id="936e1-185">-Force</span><span class="sxs-lookup"><span data-stu-id="936e1-185">-Force</span></span>

<span data-ttu-id="936e1-186">사용자 확인을 요청하지 않고 명령을 강제 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-186">Forces the command to run without asking for user confirmation.</span></span> <span data-ttu-id="936e1-187">또한, 단순하거나 짧은 컴퓨터 이름(예: 도메인 이름이 아니거나 정규화되지 않은 이름)을 입력할 경우 확인하는 메시지도 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-187">In addition, it also prompts for confirmation when you enter a simple or short computer name (such as a name that is not a domain name or is not fully qualified).</span></span> <span data-ttu-id="936e1-188">확인은 보안 때문에 필요하므로 컴퓨터가 작업 그룹에 있는 경우에만 단순 이름을 사용하여 컴퓨터를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-188">Confirmation is requested for security reasons, so that you can use the simple name to add a computer only if the computer is in a workgroup.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-189">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-189">Aliases</span></span>                              | <span data-ttu-id="936e1-190">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-190">none</span></span>                                 |
| <span data-ttu-id="936e1-191">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-191">Required?</span></span>                            | <span data-ttu-id="936e1-192">false</span><span class="sxs-lookup"><span data-stu-id="936e1-192">false</span></span>                                |
| <span data-ttu-id="936e1-193">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-193">Position?</span></span>                            | <span data-ttu-id="936e1-194">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-194">named</span></span>                                |
| <span data-ttu-id="936e1-195">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-195">Default Value</span></span>                        | <span data-ttu-id="936e1-196">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-196">none</span></span>                                 |
| <span data-ttu-id="936e1-197">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-197">Accept Pipeline Input?</span></span>               | <span data-ttu-id="936e1-198">false</span><span class="sxs-lookup"><span data-stu-id="936e1-198">false</span></span>                                |
| <span data-ttu-id="936e1-199">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-199">Accept Wildcard Characters?</span></span>          | <span data-ttu-id="936e1-200">false</span><span class="sxs-lookup"><span data-stu-id="936e1-200">false</span></span>                                |

### <a name="-rulename-string"></a><span data-ttu-id="936e1-201">-RuleName \<String\></span><span class="sxs-lookup"><span data-stu-id="936e1-201">-RuleName \<String\></span></span>

<span data-ttu-id="936e1-202">이 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-202">Specifies the friendly name for this rule.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-203">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-203">Aliases</span></span>                              | <span data-ttu-id="936e1-204">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-204">none</span></span>                                 |
| <span data-ttu-id="936e1-205">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-205">Required?</span></span>                            | <span data-ttu-id="936e1-206">false</span><span class="sxs-lookup"><span data-stu-id="936e1-206">false</span></span>                                |
| <span data-ttu-id="936e1-207">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-207">Position?</span></span>                            | <span data-ttu-id="936e1-208">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-208">named</span></span>                                |
| <span data-ttu-id="936e1-209">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-209">Default Value</span></span>                        | <span data-ttu-id="936e1-210">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-210">none</span></span>                                 |
| <span data-ttu-id="936e1-211">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-211">Accept Pipeline Input?</span></span>               | <span data-ttu-id="936e1-212">True (ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-212">True (ByPropertyName)</span></span>                |
| <span data-ttu-id="936e1-213">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-213">Accept Wildcard Characters?</span></span>          | <span data-ttu-id="936e1-214">false</span><span class="sxs-lookup"><span data-stu-id="936e1-214">false</span></span>                                |

### <a name="-usergroupname-string"></a><span data-ttu-id="936e1-215">-UserGroupName \<String\[\]\></span><span class="sxs-lookup"><span data-stu-id="936e1-215">-UserGroupName \<String\[\]\></span></span>

<span data-ttu-id="936e1-216">이 규칙이 액세스 권한을 부여하는 AD DS의 사용자 그룹 하나 이상 또는 로컬 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-216">Specifies the name of one or more user groups in AD DS or local groups to which this rule grants access.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-217">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-217">Aliases</span></span>                              | <span data-ttu-id="936e1-218">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-218">none</span></span>                                 |
| <span data-ttu-id="936e1-219">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-219">Required?</span></span>                            | <span data-ttu-id="936e1-220">true</span><span class="sxs-lookup"><span data-stu-id="936e1-220">true</span></span>                                 |
| <span data-ttu-id="936e1-221">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-221">Position?</span></span>                            | <span data-ttu-id="936e1-222">명명됨</span><span class="sxs-lookup"><span data-stu-id="936e1-222">named</span></span>                                |
| <span data-ttu-id="936e1-223">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-223">Default Value</span></span>                        | <span data-ttu-id="936e1-224">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-224">none</span></span>                                 |
| <span data-ttu-id="936e1-225">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-225">Accept Pipeline Input?</span></span>               | <span data-ttu-id="936e1-226">True (ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-226">True (ByPropertyName)</span></span>                |
| <span data-ttu-id="936e1-227">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-227">Accept Wildcard Characters?</span></span>          | <span data-ttu-id="936e1-228">false</span><span class="sxs-lookup"><span data-stu-id="936e1-228">false</span></span>                                |

### <a name="-username-string"></a><span data-ttu-id="936e1-229">-UserName \<String\[\]\></span><span class="sxs-lookup"><span data-stu-id="936e1-229">-UserName \<String\[\]\></span></span>

<span data-ttu-id="936e1-230">이 규칙이 액세스 권한을 부여하는 하나 이상의 사용자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-230">Specifies one or more users to which this rule grants access.</span></span> <span data-ttu-id="936e1-231">사용자 이름은 게이트웨이 컴퓨터의 로컬 사용자 계정 또는 AD DS의 사용자일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-231">The user name can be a local user account on the gateway computer or a user in AD DS.</span></span> <span data-ttu-id="936e1-232">형식은 `domain\user` 또는 `computer\user`입니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-232">The format is `domain\user` or `computer\user`.</span></span>

|||
|-|-|
| <span data-ttu-id="936e1-233">별칭</span><span class="sxs-lookup"><span data-stu-id="936e1-233">Aliases</span></span>                              | <span data-ttu-id="936e1-234">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-234">none</span></span>                                 |
| <span data-ttu-id="936e1-235">필수 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-235">Required?</span></span>                            | <span data-ttu-id="936e1-236">true</span><span class="sxs-lookup"><span data-stu-id="936e1-236">true</span></span>                                 |
| <span data-ttu-id="936e1-237">위치</span><span class="sxs-lookup"><span data-stu-id="936e1-237">Position?</span></span>                            | <span data-ttu-id="936e1-238">1</span><span class="sxs-lookup"><span data-stu-id="936e1-238">1</span></span>                                    |
| <span data-ttu-id="936e1-239">기본값</span><span class="sxs-lookup"><span data-stu-id="936e1-239">Default Value</span></span>                        | <span data-ttu-id="936e1-240">없음</span><span class="sxs-lookup"><span data-stu-id="936e1-240">none</span></span>                                 |
| <span data-ttu-id="936e1-241">파이프라인 입력 적용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-241">Accept Pipeline Input?</span></span>               | <span data-ttu-id="936e1-242">True (ByValue, ByPropertyName)</span><span class="sxs-lookup"><span data-stu-id="936e1-242">True (ByValue, ByPropertyName)</span></span>       |
| <span data-ttu-id="936e1-243">와일드카드 문자 허용 여부</span><span class="sxs-lookup"><span data-stu-id="936e1-243">Accept Wildcard Characters?</span></span>          | <span data-ttu-id="936e1-244">false</span><span class="sxs-lookup"><span data-stu-id="936e1-244">false</span></span>                                |

###  <a name="commonparameters"></a><span data-ttu-id="936e1-245">\<CommonParameters\></span><span class="sxs-lookup"><span data-stu-id="936e1-245">\<CommonParameters\></span></span>

<span data-ttu-id="936e1-246">이 cmdlet은 일반 매개 변수</span><span class="sxs-lookup"><span data-stu-id="936e1-246">This cmdlet supports the common parameters:</span></span>

<span data-ttu-id="936e1-247">-Verbose, -Debug, -ErrorAction, -ErrorVariable, -OutBuffer 및 -OutVariable을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-247">-Verbose, -Debug, -ErrorAction, -ErrorVariable, -OutBuffer, and -OutVariable.</span></span>
<span data-ttu-id="936e1-248">자세한 내용은 [about_CommonParameters](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_commonparameters)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="936e1-248">For more information, see [about_CommonParameters](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <a name="inputs"></a><span data-ttu-id="936e1-249">입력</span><span class="sxs-lookup"><span data-stu-id="936e1-249">INPUTS</span></span>

### <a name="string"></a><span data-ttu-id="936e1-250">문자열</span><span class="sxs-lookup"><span data-stu-id="936e1-250">String</span></span>

<span data-ttu-id="936e1-251">이 cmdlet은 문자열 또는 문자열 배열을 입력으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-251">This cmdlet accepts a string or an array of strings as input.</span></span>

### <a name="string"></a><span data-ttu-id="936e1-252">String\[\]</span><span class="sxs-lookup"><span data-stu-id="936e1-252">String\[\]</span></span>

<span data-ttu-id="936e1-253">이 cmdlet은 문자열 또는 문자열 배열을 입력으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-253">This cmdlet accepts a string or an array of strings as input.</span></span>

## <a name="outputs"></a><span data-ttu-id="936e1-254">출력</span><span class="sxs-lookup"><span data-stu-id="936e1-254">Outputs</span></span>

### <a name="microsoftmanagementpowershellwebaccesspswaauthorizationrule"></a><span data-ttu-id="936e1-255">Microsoft.Management.PowerShellWebAccess.PswaAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="936e1-255">Microsoft.Management.PowerShellWebAccess.PswaAuthorizationRule</span></span>

<span data-ttu-id="936e1-256">이 cmdlet은 권한 부여 규칙 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-256">This cmdlet returns the an authorization rule object.</span></span>

## <a name="examples"></a><span data-ttu-id="936e1-257">예제</span><span class="sxs-lookup"><span data-stu-id="936e1-257">EXAMPLES</span></span>

### <a name="example-1"></a><span data-ttu-id="936e1-258">예제 1</span><span class="sxs-lookup"><span data-stu-id="936e1-258">EXAMPLE 1</span></span>

<span data-ttu-id="936e1-259">이 예제에서는 _srv2_에서 _SMAdmins_ 그룹의 사용자에게 세션 구성 _PSWAEndpoint_(제한된 runspace)에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-259">This example grants access to the session configuration _PSWAEndpoint_, a restricted runspace, on _srv2_ for users in the _SMAdmins_ group.</span></span>

> [!NOTE]
> <span data-ttu-id="936e1-260">컴퓨터 이름은 FQDN(정규화된 도메인 이름)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-260">The computer name must be a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="936e1-261">관리자는 최종 사용자가 실행할 수 있는 제한된 범위의 cmdlet 및 작업인 제한 세션 구성 또는 runspace를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-261">Administrators define a restricted session configuration or runspace, which is a limited range of cmdlets and tasks that end users can run.</span></span> <span data-ttu-id="936e1-262">제한된 runspace를 정의하면 사용자가 허용된 Windows PowerShell(r) runspace에 없는 다른 컴퓨터에 액세스하지 못하므로 더 안전한 연결을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-262">Defining a restricted runspace can prevent users from accessing other computers that are not in the allowed Windows PowerShell(r) runspace, thus offering a more secure connection.</span></span> <span data-ttu-id="936e1-263">세션 구성에 대한 자세한 내용은 [about_Session_Configurations](/powershell/module/microsoft.powershell.core/about/about_session_configurations) 또는 [Windows PowerShell 웹 액세스 설치 및 사용](../install-and-use-windows-powershell-web-access.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="936e1-263">For more information on session configurations, see [about_Session_Configurations](/powershell/module/microsoft.powershell.core/about/about_session_configurations) or [Install and Use Windows PowerShell Web Access](../install-and-use-windows-powershell-web-access.md).</span></span>

```powershell
Add-PswaAuthorizationRule -ComputerName srv2.contoso.com -UserGroupName contoso\SMAdmins -ConfigurationName PSWAEndpoint
```

### <a name="example-2"></a><span data-ttu-id="936e1-264">예제 2</span><span class="sxs-lookup"><span data-stu-id="936e1-264">EXAMPLE 2</span></span>

<span data-ttu-id="936e1-265">이 예제에서는 *srv2*에서 `contoso\user1`, `contoso\user2` 및 `contoso\user3`이라는 사용자에게 기본 Windows PowerShell 세션 구성 `Microsoft.PowerShell`에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-265">This example grants access to the default Windows PowerShell session configuration, `Microsoft.PowerShell`, on *srv2* for users in the users named `contoso\user1`, `contoso\user2`, and `contoso\user3`.</span></span> <span data-ttu-id="936e1-266">이 cmdlet은 세 개의 규칙(사용자당 1개)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-266">This cmdlet creates three rules (1 per person).</span></span>

```powershell
Add-PswaAuthorizationRule -UserName contoso\user1, contoso\user2, contoso\user3 -ComputerName srv2.contoso.com -ConfigurationName Microsoft.PowerShell
```

### <a name="example-3"></a><span data-ttu-id="936e1-267">예제 3</span><span class="sxs-lookup"><span data-stu-id="936e1-267">EXAMPLE 3</span></span>

<span data-ttu-id="936e1-268">이 예제에서는 파이프라인을 통해 사용자 이름 값을 입력하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-268">This example illustrates how to input user name values via the pipeline.</span></span>

```powershell
"contoso\user1","contoso\user2" | Add-pswaAuthorizationRule -ComputerName srv2.contoso.com -ConfigurationName Microsoft.PowerShell
```

### <a name="example-4"></a><span data-ttu-id="936e1-269">예제 4</span><span class="sxs-lookup"><span data-stu-id="936e1-269">EXAMPLE 4</span></span>

<span data-ttu-id="936e1-270">이 예제에서는 모든 매개 변수의 값을 속성 이름별로 파이프라인에서 가져오는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-270">This example illustrates how all parameters take values from pipeline by property name.</span></span>

````powershell
$o = New-Object -TypeName PSObject |
    Add-Member -Type NoteProperty -Name "UserName" -Value "contoso\user1" -PassThru |
    Add-Member -Type NoteProperty -Name "ComputerName" -Value "srv2.contoso.com" -PassThru |
    Add-Member -Type NoteProperty -Name "ConfigurationName" -Value "Microsoft.PowerShell" -PassThru

$o | Add-PswaAuthorizationRule -UserName contoso\user1 -ConfigurationName Microsoft.PowerShell
````

### <a name="example-5"></a><span data-ttu-id="936e1-271">예제 5</span><span class="sxs-lookup"><span data-stu-id="936e1-271">EXAMPLE 5</span></span>

<span data-ttu-id="936e1-272">이 예제에서는 `PswaServer\ChrisLocal`이라는 로컬 사용자가 **srv1.contoso.com**이라는 서버에 액세스할 수 있도록 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-272">This example adds a rule to allow the local user named `PswaServer\ChrisLocal` access to the server named **srv1.contoso.com**.</span></span>

<span data-ttu-id="936e1-273">이 예제에서는 게이트웨이가 작업 그룹에 있고 대상 컴퓨터가 도메인에 있는 시나리오를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-273">This example illustrates a scenario where the gateway is in a workgroup and the destination computer is in a domain.</span></span> <span data-ttu-id="936e1-274">권한 부여 규칙은 게이트웨이의 로컬 사용자에게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-274">The authorization rule applies to the local users on the gateway.</span></span> <span data-ttu-id="936e1-275">Windows PowerShell 웹 액세스 로그인 페이지에서 인증하려면 사용자는 **옵션 연결 설정** 영역의 두 번째 자격 증명 집합을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-275">On the Windows PowerShell Web Access sign-in page, to successfully authenticate, the user must provide a second set of credentials in the **Optional connection settings** area.</span></span> <span data-ttu-id="936e1-276">게이트웨이 서버는 추가 자격 증명 집합을 사용하여 대상 컴퓨터인 *srv1.contoso.com*이라는 서버에서 사용자를 인증합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-276">The gateway server uses the additional set of credentials to authenticate the user on the destination computer, a server named *srv1.contoso.com*.</span></span>

````powershell
Add-PswaAuthorizationRule -UserName PswaServer\ChrisLocal -ComputerName srv1.contoso.com -ConfigurationName Microsoft.PowerShell
````

### <a name="example-6"></a><span data-ttu-id="936e1-277">예제 6</span><span class="sxs-lookup"><span data-stu-id="936e1-277">EXAMPLE 6</span></span>

<span data-ttu-id="936e1-278">이 예제에서는 모든 사용자가 모든 컴퓨터의 모든 엔드포인트에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-278">This example allows all users access to all endpoints on all computers.</span></span> <span data-ttu-id="936e1-279">여기서는 기본적으로 권한 부여 규칙을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-279">This essentially turns off authorization rules.</span></span>

> [!NOTE]
> <span data-ttu-id="936e1-280">`*` 와일드카드 문자는 보안이 중요한 배포에서는 사용하지 않는 것이 좋으며 테스트 환경에서나 보안을 완화할 수 있는 배포에서만 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="936e1-280">Use of the `*` wildcard character is not recommended for security-sensitive deployments and should only be considered for test environments or used in deployments where security can be relaxed.</span></span>

````powershell
Add-PswaAuthorizationRule -UserName * -ComputerName * -ConfigurationName *
````

## <a name="see-also"></a><span data-ttu-id="936e1-281">참고 항목</span><span class="sxs-lookup"><span data-stu-id="936e1-281">See Also</span></span>

<span data-ttu-id="936e1-282">[Get-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592891(v=wps.630).aspx)</span><span class="sxs-lookup"><span data-stu-id="936e1-282">[Get-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592891(v=wps.630).aspx)</span></span>

<span data-ttu-id="936e1-283">[Remove-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592893(v=wps.630).aspx)</span><span class="sxs-lookup"><span data-stu-id="936e1-283">[Remove-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592893(v=wps.630).aspx)</span></span>

<span data-ttu-id="936e1-284">[Test-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592892(v=wps.630).aspx)</span><span class="sxs-lookup"><span data-stu-id="936e1-284">[Test-PswaAuthorizationRule](https://technet.microsoft.com/library/jj592892(v=wps.630).aspx)</span></span>

<span data-ttu-id="936e1-285">[Install-PswaWebApplication](https://technet.microsoft.com/library/jj592894(v=wps.630).aspx)</span><span class="sxs-lookup"><span data-stu-id="936e1-285">[Install-PswaWebApplication](https://technet.microsoft.com/library/jj592894(v=wps.630).aspx)</span></span>

[<span data-ttu-id="936e1-286">Add-Member</span><span class="sxs-lookup"><span data-stu-id="936e1-286">Add-Member</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=113280)

[<span data-ttu-id="936e1-287">New-Object</span><span class="sxs-lookup"><span data-stu-id="936e1-287">New-Object</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=113355)

[<span data-ttu-id="936e1-288">Get-Credential</span><span class="sxs-lookup"><span data-stu-id="936e1-288">Get-Credential</span></span>](http://go.microsoft.com/fwlink/?LinkID=293936)
