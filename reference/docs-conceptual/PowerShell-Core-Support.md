# <a name="powershell-core-support-lifecycle"></a><span data-ttu-id="b7977-101">PowerShell Core 지원 수명 주기</span><span class="sxs-lookup"><span data-stu-id="b7977-101">PowerShell Core Support Lifecycle</span></span>

<span data-ttu-id="b7977-102">PowerShell Core는 Windows PowerShell과 별개로 제공, 설치 및 구성되는 도구 및 구성 요소의 고유 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-102">PowerShell Core is a distinct set of tools and components that is shipped, installed, and configured separately from Windows PowerShell.</span></span>
<span data-ttu-id="b7977-103">따라서 PowerShell Core는 Windows 7/8.1/10 또는 Windows Server 라이선싱 계약에 포함되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-103">Therefore, PowerShell Core is not included in the Windows 7/8.1/10 or Windows Server licensing agreements.</span></span>

<span data-ttu-id="b7977-104">그러나 PowerShell Core는 [프리미어][], [Microsoft 기업 계약][enterprise-agreement] 및 [Microsoft 소프트웨어 보증][assurance]을 포함한 기존의 Microsoft 지원 계약에서 지원받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-104">However, PowerShell Core is supported under traditional Microsoft support agreements, including [Premier][], [Microsoft Enterprise Agreements][enterprise-agreement], and [Microsoft Software Assurance][assurance].</span></span>
<span data-ttu-id="b7977-105">또한, 문제가 있는 경우 지원 요청서를 작성하여 PowerShell Core에 대한 [보조 지원][]을 유료로 이용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-105">You can also pay for [assisted support][] for PowerShell Core by filing a support request for your problem.</span></span>

<span data-ttu-id="b7977-106">또한 GitHub에 대한 [커뮤니티 지원][]도 제공하여 문제, 버그 또는 기능 요청을 취합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-106">We also offer [community support][] on GitHub where you can file an issue, bug, or feature request.</span></span>
<span data-ttu-id="b7977-107">또는, [Microsoft 커뮤니티][] 또는 Microsoft [PowerShell 기술 커뮤니티][]와 같은 일반적인 커뮤니티에서 다양한 구성원들에게 도움을 받을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-107">Alternatively, you may find help from other members of the community on the general [Microsoft Community][] or the Microsoft [PowerShell Tech Community][].</span></span>
<span data-ttu-id="b7977-108">단, 문제가 제때 해결된다는 보장은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-108">We offer no guarantee there that your issue will be addressed or resolved in a timely manner.</span></span>
<span data-ttu-id="b7977-109">긴급하게 도움이 필요한 문제가 있는 경우 기존의 유료 지원 옵션을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-109">If you have a problem that requires immediate attention, you should use the traditional, paid support options.</span></span>

## <a name="lifecycle-of-powershell-core"></a><span data-ttu-id="b7977-110">PowerShell Core의 수명 주기</span><span class="sxs-lookup"><span data-stu-id="b7977-110">Lifecycle of PowerShell Core</span></span>

<span data-ttu-id="b7977-111">PowerShell Core는 [Microsoft 최신 수명 주기 정책][modern]을 채택합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-111">PowerShell Core is adopting the [Microsoft Modern Lifecycle Policy][modern].</span></span>
<span data-ttu-id="b7977-112">이 지원 수명 주기는 고객이 항상 최신 버전을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-112">This support lifecycle is intended to keep customers up-to-date with the latest versions.</span></span>

<span data-ttu-id="b7977-113">약 6개월 단위로 PowerShell Core의 6.x 버전이 분기별로 업데이트 됩니다(예: 6.0, 6.1, 6.2 등).</span><span class="sxs-lookup"><span data-stu-id="b7977-113">The version 6.x branch of PowerShell Core will be updated approximately once every six months (e.g. 6.0, 6.1, 6.2, etc.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7977-114">지원을 계속 받으려면 부 버전이 새로 릴리스될 때마다 6개월 이내에 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-114">You must update within six months after each new minor version release to continue receiving support.</span></span>

<span data-ttu-id="b7977-115">예를 들어 PowerShell Core 6.1이 2018년 7월 1일에 릴리스 되고, 계속해서 지원을 받고자 하는 경우 2019년 1월 1일까지 PowerShell Core 6.1로 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-115">For example, if PowerShell Core 6.1 is released on July 1st, 2018, you would be expected to update to PowerShell Core 6.1 by January 1st, 2019 to maintain support.</span></span>

![PowerShell Core 분기 수명 주기][lifecycle-chart]

<span data-ttu-id="b7977-117">최신 수명 주기 정책에 따라 Microsoft는 해당 제품(예: PowerShell Core)에 대한 지원을 중단하기 12개월 전에 고객 측에 공지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-117">The Modern Lifecycle Policy also requires that Microsoft give customers 12 months notice before discontinuing support for a product (i.e. PowerShell Core).</span></span>

<span data-ttu-id="b7977-118">즉, PowerShell Core는 "장기 서비스"를 채택하여 6.x의 특정 분기/버전에 대한 지속적인 지원을 위해 서비스 및 보안 업데이트를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-118">Eventually, we expect PowerShell Core will adopt the "long-term servicing" approach where we would require only servicing and security updates to stay in support on a specific branch/version of 6.x.</span></span>

## <a name="supported-platforms"></a><span data-ttu-id="b7977-119">지원되는 플랫폼</span><span class="sxs-lookup"><span data-stu-id="b7977-119">Supported platforms</span></span>

<span data-ttu-id="b7977-120">사용하는 PowerShell Core 버전에 대해 공식적으로 지원되는 플랫폼에 대해서는 다음 표를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7977-120">Please see the following table to see what platform the version of PowerShell Core you are using is officially supported.</span></span>

<span data-ttu-id="b7977-121">또한 커뮤니티에서 일부 플랫폼과 관련한 패키지를 제공하였으나 공식적으로 지원되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-121">Our community has also contributed packages for some platforms, but they are not officially supported.</span></span>
<span data-ttu-id="b7977-122">이러한 패키지는 표에서 `Community`로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-122">These packages are marked as `Community` in the table.</span></span>

<span data-ttu-id="b7977-123">`Experimental`로 나열되는 플랫폼은 공식적으로 지원되지는 않지만, 실험 및 피드백용으로 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-123">Platforms listed as `Experimental` are not officially supported, but are available for experimentation and feedback.</span></span>

|                                                   | <span data-ttu-id="b7977-124">6.0</span><span class="sxs-lookup"><span data-stu-id="b7977-124">6.0</span></span>         | <span data-ttu-id="b7977-125">6.1</span><span class="sxs-lookup"><span data-stu-id="b7977-125">6.1</span></span>         |
|---------------------------------------------------|:-----------:|:-----------:|
| <span data-ttu-id="b7977-126">Windows 7, 8.1 및 10</span><span class="sxs-lookup"><span data-stu-id="b7977-126">Windows 7, 8.1, and 10</span></span>                            | <span data-ttu-id="b7977-127">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-127">Supported</span></span>   | <span data-ttu-id="b7977-128">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-128">Supported</span></span>   |
| <span data-ttu-id="b7977-129">Windows Server 2008 R2, 2012 R2, 2016</span><span class="sxs-lookup"><span data-stu-id="b7977-129">Windows Server 2008 R2, 2012 R2, 2016</span></span>             | <span data-ttu-id="b7977-130">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-130">Supported</span></span>   | <span data-ttu-id="b7977-131">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-131">Supported</span></span>   |
| <span data-ttu-id="b7977-132">[Windows 서버 반기 채널][semi-annual]</span><span class="sxs-lookup"><span data-stu-id="b7977-132">[Windows Server Semi-Annual Channel][semi-annual]</span></span> | <span data-ttu-id="b7977-133">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-133">Supported</span></span>   | <span data-ttu-id="b7977-134">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-134">Supported</span></span>   |
| <span data-ttu-id="b7977-135">Ubuntu 14.04, 16.04</span><span class="sxs-lookup"><span data-stu-id="b7977-135">Ubuntu 14.04 and, 16.04</span></span>                           | <span data-ttu-id="b7977-136">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-136">Supported</span></span>   | <span data-ttu-id="b7977-137">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-137">Supported</span></span>   |
| <span data-ttu-id="b7977-138">Ubuntu 17.10, 18.04</span><span class="sxs-lookup"><span data-stu-id="b7977-138">Ubuntu 17.10, and 18.04</span></span>                           |             | <span data-ttu-id="b7977-139">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-139">Supported</span></span>   |
| <span data-ttu-id="b7977-140">Debian 8.7+, 9</span><span class="sxs-lookup"><span data-stu-id="b7977-140">Debian 8.7+, and 9</span></span>                                | <span data-ttu-id="b7977-141">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-141">Supported</span></span>   | <span data-ttu-id="b7977-142">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-142">Supported</span></span>   |
| <span data-ttu-id="b7977-143">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="b7977-143">CentOS 7</span></span>                                          | <span data-ttu-id="b7977-144">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-144">Supported</span></span>   | <span data-ttu-id="b7977-145">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-145">Supported</span></span>   |
| <span data-ttu-id="b7977-146">Red Hat Enterprise Linux 7</span><span class="sxs-lookup"><span data-stu-id="b7977-146">Red Hat Enterprise Linux 7</span></span>                        | <span data-ttu-id="b7977-147">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-147">Supported</span></span>   | <span data-ttu-id="b7977-148">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-148">Supported</span></span>   |
| <span data-ttu-id="b7977-149">OpenSUSE 42.2</span><span class="sxs-lookup"><span data-stu-id="b7977-149">OpenSUSE 42.2</span></span>                                     | <span data-ttu-id="b7977-150">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-150">Supported</span></span>   | <span data-ttu-id="b7977-151">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-151">Supported</span></span>   |
| <span data-ttu-id="b7977-152">Fedora 27</span><span class="sxs-lookup"><span data-stu-id="b7977-152">Fedora 27</span></span>                                         | <span data-ttu-id="b7977-153">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-153">Supported</span></span>   | <span data-ttu-id="b7977-154">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-154">Supported</span></span>   |
| <span data-ttu-id="b7977-155">Fedora 28</span><span class="sxs-lookup"><span data-stu-id="b7977-155">Fedora 28</span></span>                                         |             | <span data-ttu-id="b7977-156">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-156">Supported</span></span>   |
| <span data-ttu-id="b7977-157">macOS 10.12+</span><span class="sxs-lookup"><span data-stu-id="b7977-157">macOS 10.12+</span></span>                                      | <span data-ttu-id="b7977-158">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-158">Supported</span></span>   | <span data-ttu-id="b7977-159">지원 여부</span><span class="sxs-lookup"><span data-stu-id="b7977-159">Supported</span></span>   |
| <span data-ttu-id="b7977-160">Arch</span><span class="sxs-lookup"><span data-stu-id="b7977-160">Arch</span></span>                                              | <span data-ttu-id="b7977-161">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-161">Community</span></span>   | <span data-ttu-id="b7977-162">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-162">Community</span></span>   |
| <span data-ttu-id="b7977-163">Raspbian</span><span class="sxs-lookup"><span data-stu-id="b7977-163">Raspbian</span></span>                                          | <span data-ttu-id="b7977-164">실험적</span><span class="sxs-lookup"><span data-stu-id="b7977-164">Experimental</span></span>| <span data-ttu-id="b7977-165">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-165">Community</span></span>   |
| <span data-ttu-id="b7977-166">Kali</span><span class="sxs-lookup"><span data-stu-id="b7977-166">Kali</span></span>                                              | <span data-ttu-id="b7977-167">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-167">Community</span></span>   | <span data-ttu-id="b7977-168">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-168">Community</span></span>   |
| <span data-ttu-id="b7977-169">AppImage(여러 Linux 플랫폼에서 사용)</span><span class="sxs-lookup"><span data-stu-id="b7977-169">AppImage  (works on multiple Linux platforms)</span></span>     | <span data-ttu-id="b7977-170">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-170">Community</span></span>   | <span data-ttu-id="b7977-171">커뮤니티</span><span class="sxs-lookup"><span data-stu-id="b7977-171">Community</span></span>   |

## <a name="platform-which-are-out-of-support"></a><span data-ttu-id="b7977-172">지원되지 않는 플랫폼</span><span class="sxs-lookup"><span data-stu-id="b7977-172">Platform which are out of support</span></span>

<span data-ttu-id="b7977-173">플랫폼 버전이 플랫폼 소유자가 정의한 수명 종료에 도달하면 PowerShell Core도 해당 플랫폼 버전에 대한 지원 제공을 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-173">When a platform version reaches end-of-life as defined by the platform owner, PowerShell Core will also cease to provide support for that platform version.</span></span> <span data-ttu-id="b7977-174">이전에 릴리스된 패키지는 액세스가 필요한 고객이 계속 사용할 수는 있지만, 공식 지원 및 업데이트는 더 이상 제공되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-174">Previously released packages will remain available for customers needing access but formal support and updates of any kind will no longer be provided.</span></span>

<span data-ttu-id="b7977-175">그러므로 다음 버전에 대한 지원은 배포 소유자가 종료했으며, 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-175">Therefore, support for the following versions was ended by the distribution owners and are not supported.</span></span>

| <span data-ttu-id="b7977-176">OS</span><span class="sxs-lookup"><span data-stu-id="b7977-176">OS</span></span>       | <span data-ttu-id="b7977-177">버전</span><span class="sxs-lookup"><span data-stu-id="b7977-177">Version</span></span> | <span data-ttu-id="b7977-178">수명 종료</span><span class="sxs-lookup"><span data-stu-id="b7977-178">End of Life</span></span>                                                                                 |
|----------|---------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7977-179">Fedora</span><span class="sxs-lookup"><span data-stu-id="b7977-179">Fedora</span></span>   | <span data-ttu-id="b7977-180">26</span><span class="sxs-lookup"><span data-stu-id="b7977-180">26</span></span>      | [<span data-ttu-id="b7977-181">2018년 5월</span><span class="sxs-lookup"><span data-stu-id="b7977-181">May 2018</span></span>](https://fedoramagazine.org/fedora-26-end-life/)                                  |
| <span data-ttu-id="b7977-182">Fedora</span><span class="sxs-lookup"><span data-stu-id="b7977-182">Fedora</span></span>   | <span data-ttu-id="b7977-183">25</span><span class="sxs-lookup"><span data-stu-id="b7977-183">25</span></span>      | [<span data-ttu-id="b7977-184">2017년 12월</span><span class="sxs-lookup"><span data-stu-id="b7977-184">December 2017</span></span>](https://fedoramagazine.org/fedora-25-end-life/)                             |
| <span data-ttu-id="b7977-185">Fedora</span><span class="sxs-lookup"><span data-stu-id="b7977-185">Fedora</span></span>   | <span data-ttu-id="b7977-186">24</span><span class="sxs-lookup"><span data-stu-id="b7977-186">24</span></span>      | [<span data-ttu-id="b7977-187">2017년 8월</span><span class="sxs-lookup"><span data-stu-id="b7977-187">August 2017</span></span>](https://fedoramagazine.org/fedora-24-eol/)                                    |
| <span data-ttu-id="b7977-188">openSUSE</span><span class="sxs-lookup"><span data-stu-id="b7977-188">openSUSE</span></span> | <span data-ttu-id="b7977-189">42.2</span><span class="sxs-lookup"><span data-stu-id="b7977-189">42.2</span></span>    | [<span data-ttu-id="b7977-190">2018년 1월</span><span class="sxs-lookup"><span data-stu-id="b7977-190">January 2018</span></span>](https://lists.opensuse.org/opensuse-security-announce/2017-11/msg00066.html) |
| <span data-ttu-id="b7977-191">openSUSE</span><span class="sxs-lookup"><span data-stu-id="b7977-191">openSUSE</span></span> | <span data-ttu-id="b7977-192">42.1</span><span class="sxs-lookup"><span data-stu-id="b7977-192">42.1</span></span>    | [<span data-ttu-id="b7977-193">2017년 5월</span><span class="sxs-lookup"><span data-stu-id="b7977-193">May 2017</span></span>](https://lists.opensuse.org/opensuse-security-announce/2017-05/msg00053.html)     |
| <span data-ttu-id="b7977-194">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b7977-194">Ubuntu</span></span>   | <span data-ttu-id="b7977-195">17.04</span><span class="sxs-lookup"><span data-stu-id="b7977-195">17.04</span></span>   | [<span data-ttu-id="b7977-196">2018년 1월</span><span class="sxs-lookup"><span data-stu-id="b7977-196">January 2018</span></span>](https://lists.ubuntu.com/archives/ubuntu-announce/2018-January.txt)          |
| <span data-ttu-id="b7977-197">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b7977-197">Ubuntu</span></span>   | <span data-ttu-id="b7977-198">16.10</span><span class="sxs-lookup"><span data-stu-id="b7977-198">16.10</span></span>   | [<span data-ttu-id="b7977-199">2017년 7월</span><span class="sxs-lookup"><span data-stu-id="b7977-199">July 2017</span></span>](https://lists.ubuntu.com/archives/ubuntu-announce/2017-July/000223.html)        |

## <a name="notes-on-licensing"></a><span data-ttu-id="b7977-200">라이선싱에 대한 메모</span><span class="sxs-lookup"><span data-stu-id="b7977-200">Notes on licensing</span></span>

<span data-ttu-id="b7977-201">PowerShell Core는 [MIT 라이선스][]에서 릴리스 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-201">PowerShell Core is released under the [MIT license][].</span></span>
<span data-ttu-id="b7977-202">본 라이선스 및 유료 지원 계약이 안 된 경우 사용자는 [커뮤니티 지원][]으로 서비스가 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-202">Under this license, and in the absence of a paid support agreement, users are limited to [community support][].</span></span>
<span data-ttu-id="b7977-203">커뮤니티 지원을 이용하더라도 Microsoft는 문의 응답 및 해결 방안을 보장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-203">With community support, Microsoft makes no guarantees of responsiveness or fixes.</span></span>

## <a name="windows-powershell-module"></a><span data-ttu-id="b7977-204">Windows PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="b7977-204">Windows PowerShell Module</span></span>

<span data-ttu-id="b7977-205">PowerShell Core에 대한 지원은 명시적으로 이 모듈이 PowerShell Core를 지원하지 않는 한 다른 제품 모듈로 확장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-205">Support for PowerShell Core does not extend to other product modules unless those modules explicitly support PowerShell Core.</span></span>
<span data-ttu-id="b7977-206">예를 들어, Windows Server에 부분적으로 제공되는 `ActiveDirectory` 모듈을 사용하는 경우 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-206">For example, using the `ActiveDirectory` module that ships as part of Windows Server is an unsupported scenario.</span></span>

<span data-ttu-id="b7977-207">그러나 PowerShell Core를 명시적으로 지원하지 않는 모듈은 경우에 따라 호환이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-207">However, modules that do not explicitly support PowerShell Core may be compatible in some cases.</span></span>
<span data-ttu-id="b7977-208">[`WindowsPSModulePath`][] 모듈을 설치하여 Windows PowerShell `PSModulePath` 를 PowerShell Core `PSModulePath`로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-208">By installing the [`WindowsPSModulePath`][] module, you can append the Windows PowerShell `PSModulePath` to your PowerShell Core `PSModulePath`.</span></span>

<span data-ttu-id="b7977-209">먼저, PowerShell 갤러리에서 `WindowsPSModulePath` 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-209">First, install the `WindowsPSModulePath` module from the PowerShell Gallery:</span></span>

```powershell
# Add `-Scope CurrentUser` if you're installing as non-admin
Install-Module WindowsPSModulePath -Force
```

<span data-ttu-id="b7977-210">이 모듈을 설치한 후에, `Add-WindowsPSModulePath` cmdlet을 실행하여 Windows PowerShell `PSModulePath`를 PowerShell Core에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b7977-210">After installing this module, run the `Add-WindowsPSModulePath` cmdlet to add the Windows PowerShell `PSModulePath` to PowerShell Core:</span></span>

```powershell
# Add this line to your profile if you always want Windows PowerShell PSModulePath
Add-WindowsPSModulePath
```

[프리미어]: https://www.microsoft.com/en-us/microsoftservices/support.aspx
[Premier]: https://www.microsoft.com/en-us/microsoftservices/support.aspx
[enterprise-agreement]: https://www.microsoft.com/en-us/licensing/licensing-programs/enterprise.aspx
[assurance]: https://www.microsoft.com/en-us/licensing/licensing-programs/software-assurance-default.aspx
[커뮤니티 지원]: https://github.com/powershell/powershell/issues
[community support]: https://github.com/powershell/powershell/issues
[Microsoft 커뮤니티]: https://answers.microsoft.com/
[Microsoft Community]: https://answers.microsoft.com/
[PowerShell 기술 커뮤니티]: https://techcommunity.microsoft.com/t5/PowerShell/ct-p/WindowsPowerShell
[PowerShell Tech Community]: https://techcommunity.microsoft.com/t5/PowerShell/ct-p/WindowsPowerShell
[보조 지원]: https://support.microsoft.com/assistedsupportproducts
[assisted support]: https://support.microsoft.com/assistedsupportproducts
[modern]: https://support.microsoft.com/help/30881/modern-lifecycle-policy
[lifecycle-chart]: ./images/modern-lifecycle.png
[semi-annual]: https://docs.microsoft.com/windows-server/get-started/semi-annual-channel-overview
[MIT 라이선스]: https://github.com/PowerShell/PowerShell/blob/master/LICENSE.txt
[MIT license]: https://github.com/PowerShell/PowerShell/blob/master/LICENSE.txt
[`WindowsPSModulePath`]: https://www.powershellgallery.com/packages/WindowsPSModulePath/
