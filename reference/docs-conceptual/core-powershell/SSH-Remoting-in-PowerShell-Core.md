
# <a name="powershell-remoting-over-ssh"></a><span data-ttu-id="56dcd-101">SSH를 통한 PowerShell 원격</span><span class="sxs-lookup"><span data-stu-id="56dcd-101">PowerShell Remoting Over SSH</span></span>

## <a name="overview"></a><span data-ttu-id="56dcd-102">개요</span><span class="sxs-lookup"><span data-stu-id="56dcd-102">Overview</span></span>

<span data-ttu-id="56dcd-103">PowerShell 원격 기능은 일반적으로 연결 협상 및 데이터 전송에 WinRM을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-103">PowerShell remoting normally uses WinRM for connection negotiation and data transport.</span></span>
<span data-ttu-id="56dcd-104">SSH는 이제 Linux 및 Windows 플랫폼에 모두 사용할 수 있고 진정한 다중 플랫폼 PowerShell 원격 기능을 허용하므로 이 원격 기능 구현에 선택되었습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-104">SSH was chosen for this remoting implementation since it is now available for both Linux and Windows platforms and allows true multiplatform PowerShell remoting.</span></span>
<span data-ttu-id="56dcd-105">그러나 WinRM은 이 구현이 아직 지원하지 않는 PowerShell 원격 세션에 대한 강력한 호스팅 모델도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-105">However, WinRM also provides a robust hosting model for PowerShell remote sessions which this implementation does not yet do.</span></span>
<span data-ttu-id="56dcd-106">그리고 이는 PowerShell 원격 엔드포인트 구성 및 JEA(Just Enough Administration)가 이 구현에서 아직 지원되지 않음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-106">And this means that PowerShell remote endpoint configuration and JEA (Just Enough Administration) is not yet supported in this implementation.</span></span>

<span data-ttu-id="56dcd-107">PowerShell SSH 원격 기능을 사용하면 Windows 및 Linux 컴퓨터 간에 기본적인 PowerShell 세션 원격 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-107">PowerShell SSH remoting lets you do basic PowerShell session remoting between Windows and Linux machines.</span></span>
<span data-ttu-id="56dcd-108">이러한 작업은 SSH 하위 시스템인 대상 컴퓨터에 PowerShell 호스팅 프로세스를 만드는 방식으로 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-108">This is done by creating a PowerShell hosting process on the target machine as an SSH subsystem.</span></span>
<span data-ttu-id="56dcd-109">결국 이는 엔드포인트 구성 및 JEA를 지원하기 위해 WinRM이 작동하는 방식과 유사한, 보다 일반적인 호스팅 모델로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-109">Eventually this will be changed to a more general hosting model similar to how WinRM works in order to support endpoint configuration and JEA.</span></span>

<span data-ttu-id="56dcd-110">`New-PSSession`, `Enter-PSSession` 및 `Invoke-Command` cmdlet에는 이제 이 새로운 원격 연결을 용이하게 하는 새로운 매개 변수가 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-110">The `New-PSSession`, `Enter-PSSession` and `Invoke-Command` cmdlets now have a new parameter set to facilitate this new remoting connection</span></span>

```
[-HostName <string>]  [-UserName <string>]  [-KeyFilePath <string>]
```

<span data-ttu-id="56dcd-111">이 새로운 매개 변수 집합은 변경될 가능성이 높지만 현재는 명령줄에서 상호 작용하거나 명령 및 스크립트를 호출할 수 있는 SSH PSSession을 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-111">This new parameter set will likely change but for now allows you to create SSH PSSessions that you can interact with from the command line or invoke commands and scripts on.</span></span>
<span data-ttu-id="56dcd-112">HostName 매개 변수를 사용하여 대상 컴퓨터를 지정하고 UserName을 사용하여 사용자 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-112">You specify the target machine with the HostName parameter and provide the user name with UserName.</span></span>
<span data-ttu-id="56dcd-113">PowerShell 명령줄에서 대화형으로 cmdlet을 실행할 때는 암호를 묻는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-113">When running the cmdlets interactively at the PowerShell command line you will be prompted for a password.</span></span>
<span data-ttu-id="56dcd-114">하지만 SSH 키 인증을 사용하고 KeyFilePath 매개 변수를 사용하여 개인 키 파일 경로를 지정하는 옵션도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-114">But you also have the option to use SSH key authentication and provide a private key file path with the KeyFilePath parameter.</span></span>

## <a name="general-setup-information"></a><span data-ttu-id="56dcd-115">일반적인 설치 정보</span><span class="sxs-lookup"><span data-stu-id="56dcd-115">General setup information</span></span>

<span data-ttu-id="56dcd-116">SSH는 모든 컴퓨터에 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-116">SSH is required to be installed on all machines.</span></span>
<span data-ttu-id="56dcd-117">컴퓨터에서 들어오고 나가는 원격 작업을 실험할 수 있도록 클라이언트(`ssh.exe`) 및 서버(`sshd.exe`)를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-117">You should install both client (`ssh.exe`) and server (`sshd.exe`) so that you can experiment with remoting to and from the machines.</span></span>
<span data-ttu-id="56dcd-118">Windows의 경우 [GitHub의 Win32 OpenSSH](https://github.com/PowerShell/Win32-OpenSSH/releases)를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-118">For Windows you will need to install [Win32 OpenSSH from GitHub](https://github.com/PowerShell/Win32-OpenSSH/releases).</span></span>
<span data-ttu-id="56dcd-119">Linux의 경우 플랫폼에 적합한 SSH(sshd 서버 포함)를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-119">For Linux you will need to install SSH (including sshd server) appropriate to your platform.</span></span>
<span data-ttu-id="56dcd-120">또한 GitHub에서 SSH 원격 기능이 있는 최신 PowerShell 빌드 또는 패키지를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-120">You will also need a recent PowerShell build or package from GitHub having the SSH remoting feature.</span></span>
<span data-ttu-id="56dcd-121">SSH 하위 시스템은 원격 컴퓨터에 PowerShell 프로세스를 설정하는 데 사용되며, SSH 서버에 이를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-121">SSH subsystems is used to establish a PowerShell process on the remote machine and the SSH server will need to be configured for that.</span></span>
<span data-ttu-id="56dcd-122">또한 암호 인증을 활성화하고, 필요에 따라 키 기반 인증도 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-122">In addition you will need to enable password authentication and optionally key based authentication.</span></span>

## <a name="setup-on-windows-machine"></a><span data-ttu-id="56dcd-123">Windows 컴퓨터에 설치</span><span class="sxs-lookup"><span data-stu-id="56dcd-123">Setup on Windows Machine</span></span>

1. <span data-ttu-id="56dcd-124">최신 버전의 [PowerShell Core for Windows] 설치</span><span class="sxs-lookup"><span data-stu-id="56dcd-124">Install the latest version of [PowerShell Core for Windows]</span></span>
   - <span data-ttu-id="56dcd-125">`New-PSSession`의 매개 변수 집합을 확인하면 SSH 원격 기능이 지원되는지 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-125">You can tell if it has the SSH remoting support by looking at the parameter sets for `New-PSSession`</span></span>

   ```powershell
   Get-Command New-PSSession -syntax
   ```

   ```output
   New-PSSession [-HostName] <string[]> [-Name <string[]>] [-UserName <string>] [-KeyFilePath <string>] [-SSHTransport] [<CommonParameters>]
   ```

2. <span data-ttu-id="56dcd-126">[설치] 지침에 따라 GitHub에서 최신 [Win32 OpenSSH] 빌드를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-126">Install the latest [Win32 OpenSSH] build from GitHub using the [installation] instructions</span></span>
3. <span data-ttu-id="56dcd-127">Win32 OpenSSH를 설치한 위치에서 sshd_config 파일을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-127">Edit the sshd_config file at the location where you installed Win32 OpenSSH</span></span>
   - <span data-ttu-id="56dcd-128">암호 인증이 활성화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-128">Make sure password authentication is enabled</span></span>

   ```
   PasswordAuthentication yes
   ```

    ```
    Subsystem    powershell c:/program files/powershell/6.0.0/pwsh.exe -sshs -NoLogo -NoProfile
    ```

    > [!NOTE]
    <span data-ttu-id="56dcd-129">하위 시스템 실행 파일 경로의 작업에서 공백을 방지하는 Windows용 OpenSSH에 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-129">There is a bug in OpenSSH for Windows that prevents spaces from working in subsystem executable paths.</span></span>
    <span data-ttu-id="56dcd-130">[자세한 내용은 GitHub에서 이 문제](https://github.com/PowerShell/Win32-OpenSSH/issues/784)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="56dcd-130">See [this issue on GitHub for more information](https://github.com/PowerShell/Win32-OpenSSH/issues/784).</span></span>

    <span data-ttu-id="56dcd-131">한 가지 해결 방법은 공백을 포함하지 않는 Powershell 설치 디렉터리에 symlink를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-131">One solution is to create a symlink to the Powershell installation directory that does not contain spaces:</span></span>

    ```powershell
    mklink /D c:\pwsh "C:\Program Files\PowerShell\6.0.0"
    ```

    <span data-ttu-id="56dcd-132">그런 다음, 하위 시스템에 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-132">and then enter it in the subsystem:</span></span>

    ```
    Subsystem    powershell c:\pwsh\pwsh.exe -sshs -NoLogo -NoProfile
    ```

   ```
   Subsystem    powershell c:/program files/powershell/6.0.0/pwsh.exe -sshs -NoLogo -NoProfile
   ```

   - <span data-ttu-id="56dcd-133">필요에 따라 키 인증을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-133">Optionally enable key authentication</span></span>

   ```
   PubkeyAuthentication yes
   ```

4. <span data-ttu-id="56dcd-134">sshd 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-134">Restart the sshd service</span></span>

   ```powershell
   Restart-Service sshd
   ```

5. <span data-ttu-id="56dcd-135">Path Env 변수에 OpenSSH가 설치된 경로를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-135">Add the path where OpenSSH is installed to your Path Env Variable</span></span>
   - <span data-ttu-id="56dcd-136">이는 `C:\Program Files\OpenSSH\` 줄에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-136">This should be along the lines of `C:\Program Files\OpenSSH\`</span></span>
   - <span data-ttu-id="56dcd-137">그래야 시스템에서 ssh.exe를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-137">This allows for the ssh.exe to be found</span></span>

## <a name="setup-on-linux-ubuntu-1404-machine"></a><span data-ttu-id="56dcd-138">Linux(Ubuntu 14.04) 컴퓨터에 설치</span><span class="sxs-lookup"><span data-stu-id="56dcd-138">Setup on Linux (Ubuntu 14.04) Machine</span></span>

1. <span data-ttu-id="56dcd-139">GitHub에서 최신 [Linux용 PowerShell Core] 빌드를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-139">Install the latest [PowerShell Core for Linux] build from GitHub</span></span>
2. <span data-ttu-id="56dcd-140">필요에 따라 [Ubuntu SSH]를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-140">Install [Ubuntu SSH] as needed</span></span>

   ```bash
   sudo apt install openssh-client
   sudo apt install openssh-server
   ```

3. <span data-ttu-id="56dcd-141">/etc/ssh 위치에서 sshd_config 파일을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-141">Edit the sshd_config file at location /etc/ssh</span></span>
   - <span data-ttu-id="56dcd-142">암호 인증이 활성화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-142">Make sure password authentication is enabled</span></span>

   ```
   PasswordAuthentication yes
   ```

   - <span data-ttu-id="56dcd-143">PowerShell 하위 시스템 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-143">Add a PowerShell subsystem entry</span></span>

   ```
   Subsystem powershell /usr/bin/pwsh -sshs -NoLogo -NoProfile
   ```

   - <span data-ttu-id="56dcd-144">필요에 따라 키 인증을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-144">Optionally enable key authentication</span></span>

   ```
   PubkeyAuthentication yes
   ```

4. <span data-ttu-id="56dcd-145">sshd 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-145">Restart the sshd service</span></span>

   ```bash
   sudo service sshd restart
   ```

## <a name="setup-on-macos-machine"></a><span data-ttu-id="56dcd-146">MacOS 컴퓨터에 설치</span><span class="sxs-lookup"><span data-stu-id="56dcd-146">Setup on MacOS Machine</span></span>

1. <span data-ttu-id="56dcd-147">최신 [MacOS용 PowerShell Core] 빌드를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-147">Install the latest [PowerShell Core for MacOS] build</span></span>
   - <span data-ttu-id="56dcd-148">다음 단계를 수행하여 SSH 원격 기능이 활성화되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-148">Make sure SSH Remoting is enabled by following these steps:</span></span>
     - <span data-ttu-id="56dcd-149">`System Preferences`를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-149">Open `System Preferences`</span></span>
     - <span data-ttu-id="56dcd-150">`Sharing`을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-150">Click on `Sharing`</span></span>
     - <span data-ttu-id="56dcd-151">`Remote Login`을 확인합니다(`Remote Login: On`이어야 함).</span><span class="sxs-lookup"><span data-stu-id="56dcd-151">Check `Remote Login` - Should say `Remote Login: On`</span></span>
     - <span data-ttu-id="56dcd-152">적절한 사용자에게 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-152">Allow access to appropriate users</span></span>
2. <span data-ttu-id="56dcd-153">`/private/etc/ssh/sshd_config` 위치에서 `sshd_config` 파일을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-153">Edit the `sshd_config` file at location `/private/etc/ssh/sshd_config`</span></span>
   - <span data-ttu-id="56dcd-154">선호하는 편집기를 사용합니다. 또는</span><span class="sxs-lookup"><span data-stu-id="56dcd-154">Use your favorite editor or</span></span>

     ```bash
     sudo nano /private/etc/ssh/sshd_config
     ```

   - <span data-ttu-id="56dcd-155">암호 인증이 활성화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-155">Make sure password authentication is enabled</span></span>

     ```
     PasswordAuthentication yes
     ```

   - <span data-ttu-id="56dcd-156">PowerShell 하위 시스템 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-156">Add a PowerShell subsystem entry</span></span>

     ```
     Subsystem powershell /usr/local/bin/pwsh -sshs -NoLogo -NoProfile
     ```

   - <span data-ttu-id="56dcd-157">필요에 따라 키 인증을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-157">Optionally enable key authentication</span></span>

     ```
     PubkeyAuthentication yes
     ```

3. <span data-ttu-id="56dcd-158">sshd 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-158">Restart the sshd service</span></span>

   ```bash
   sudo launchctl stop com.openssh.sshd
   sudo launchctl start com.openssh.sshd
   ```

## <a name="powershell-remoting-example"></a><span data-ttu-id="56dcd-159">PowerShell 원격 기능 예제</span><span class="sxs-lookup"><span data-stu-id="56dcd-159">PowerShell Remoting Example</span></span>

<span data-ttu-id="56dcd-160">원격 기능을 테스트하는 가장 쉬운 방법은 단일 컴퓨터에서 사용해 보는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-160">The easiest way to test remoting is to just try it on a single machine.</span></span>
<span data-ttu-id="56dcd-161">여기에서는 Linux 상자의 동일한 컴퓨터에 다시 원격 세션을 만들겠습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-161">Here I will create a remote session back to the same machine on a Linux box.</span></span>
<span data-ttu-id="56dcd-162">암호 프롬프트뿐만 아니라 명령 프롬프트에서도 PowerShell cmdlet을 사용하므로 SSH에서 호스트 컴퓨터를 확인할지 묻는 메시지를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-162">Notice that I am using PowerShell cmdlets from a command prompt so we see prompts from SSH asking to verify the host computer as well as password prompts.</span></span>
<span data-ttu-id="56dcd-163">또한 Windows 컴퓨터에서도 동일한 작업을 수행하여 원격 기능이 작동하는지 확인한 후 호스트 이름을 변경하여 컴퓨터 간에 원격 기능이 작동하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-163">You can do the same thing on a Windows machine to ensure remoting is working there and then remote between machines by simply changing the host name.</span></span>

```powershell
#
# Linux to Linux
#
$session = New-PSSession -HostName UbuntuVM1 -UserName TestUser
```

```output
The authenticity of host 'UbuntuVM1 (9.129.17.107)' cannot be established.
ECDSA key fingerprint is SHA256:2kCbnhT2dUE6WCGgVJ8Hyfu1z2wE4lifaJXLO7QJy0Y.
Are you sure you want to continue connecting (yes/no)?
TestUser@UbuntuVM1s password:
```

```powershell
$session
```

```output
 Id Name            ComputerName    ComputerType    State         ConfigurationName     Availability
 -- ----            ------------    ------------    -----         -----------------     ------------
  1 SSH1            UbuntuVM1       RemoteMachine   Opened        DefaultShell             Available
```

```powershell
Enter-PSSession $session
```

```output
[UbuntuVM1]: PS /home/TestUser> uname -a
Linux TestUser-UbuntuVM1 4.2.0-42-generic 49~14.04.1-Ubuntu SMP Wed Jun 29 20:22:11 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux

[UbuntuVM1]: PS /home/TestUser> Exit-PSSession
```

```powershell
Invoke-Command $session -ScriptBlock { Get-Process powershell }
```

```output
Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName                    PSComputerName
-------  ------    -----      -----     ------     --  -- -----------                    --------------
      0       0        0         19       3.23  10635 635 powershell                     UbuntuVM1
      0       0        0         21       4.92  11033 017 powershell                     UbuntuVM1
      0       0        0         20       3.07  11076 076 powershell                     UbuntuVM1
```

```powershell
#
# Linux to Windows
#
Enter-PSSession -HostName WinVM1 -UserName PTestName
```

```output
PTestName@WinVM1s password:
```

```powershell
[WinVM1]: PS C:\Users\PTestName\Documents> cmd /c ver
```

```output
Microsoft Windows [Version 10.0.10586]
```

```powershell
#
# Windows to Windows
#
C:\Users\PSUser\Documents>pwsh.exe
```

```output
PowerShell
Copyright (c) Microsoft Corporation. All rights reserved.
```

```powershell
$session = New-PSSession -HostName WinVM2 -UserName PSRemoteUser
```

```output
The authenticity of host 'WinVM2 (10.13.37.3)' can't be established.
ECDSA key fingerprint is SHA256:kSU6slAROyQVMEynVIXAdxSiZpwDBigpAF/TXjjWjmw.
Are you sure you want to continue connecting (yes/no)?
Warning: Permanently added 'WinVM2,10.13.37.3' (ECDSA) to the list of known hosts.
PSRemoteUser@WinVM2's password:
```

```powershell
$session
```

```output
 Id Name            ComputerName    ComputerType    State         ConfigurationName     Availability
 -- ----            ------------    ------------    -----         -----------------     ------------
  1 SSH1            WinVM2          RemoteMachine   Opened        DefaultShell             Available
```

```powershell
Enter-PSSession -Session $session
```

```output
[WinVM2]: PS C:\Users\PSRemoteUser\Documents> $PSVersionTable

Name                           Value
----                           -----
PSEdition                      Core
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
SerializationVersion           1.1.0.1
BuildVersion                   3.0.0.0
CLRVersion
PSVersion                      6.0.0-alpha
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
GitCommitId                    v6.0.0-alpha.17


[WinVM2]: PS C:\Users\PSRemoteUser\Documents>
```

### <a name="known-issues"></a><span data-ttu-id="56dcd-164">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="56dcd-164">Known Issues</span></span>

- <span data-ttu-id="56dcd-165">sudo 명령은 Linux 컴퓨터에 대한 원격 세션에서 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56dcd-165">sudo command does not work in remote session to Linux machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="56dcd-166">참고 항목</span><span class="sxs-lookup"><span data-stu-id="56dcd-166">See Also</span></span>

[<span data-ttu-id="56dcd-167">Windows용 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="56dcd-167">PowerShell Core for Windows</span></span>](../setup/installing-powershell-core-on-windows.md#msi)

[<span data-ttu-id="56dcd-168">Linux용 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="56dcd-168">PowerShell Core for Linux</span></span>](../setup/installing-powershell-core-on-linux.md#ubuntu-1404)

[<span data-ttu-id="56dcd-169">MacOS용 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="56dcd-169">PowerShell Core for MacOS</span></span>](../setup/installing-powershell-core-on-macos.md)

[<span data-ttu-id="56dcd-170">Win32 OpenSSH</span><span class="sxs-lookup"><span data-stu-id="56dcd-170">Win32 OpenSSH</span></span>](https://github.com/PowerShell/Win32-OpenSSH/releases)

[<span data-ttu-id="56dcd-171">설치</span><span class="sxs-lookup"><span data-stu-id="56dcd-171">installation</span></span>](https://github.com/PowerShell/Win32-OpenSSH/wiki/Install-Win32-OpenSSH)

[<span data-ttu-id="56dcd-172">Ubuntu SSH</span><span class="sxs-lookup"><span data-stu-id="56dcd-172">Ubuntu SSH</span></span>](https://help.ubuntu.com/lts/serverguide/openssh-server.html)