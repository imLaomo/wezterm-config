# Installation

```powershell
# windows powershell

## winget
winget install JanDeDobbeleer.OhMyPosh -s winget

## scoop
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json

## manual
Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))

## chocolatey
choco install oh-my-posh
```

# Configuration

```powershell
# windows powershell

## 安装图标模块
Install-Module -Name Terminal-Icons -Repository PSGallery
### Fonts recommend `Meslo LGM NF`

## 建立配置文件
New-Item -Path $PROFILE -Type File -Force
```

```powershell
oh-my-posh --init --shell pwsh --config "$env:POSH_THEMES_PATH\craver.omp.json" | Invoke-Expression

Import-Module -Name Terminal-Icons


Set-Alias -Name grep -Value Select-String
Set-alias "npp" "C:\Users\user\scoop\shims\notepad++.exe"
Set-Alias "touch" "ni"


# start the ssh-agent in the background | github
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent


# disable the .NET telemetry | https://learn.microsoft.com/zh-cn/dotnet/core/tools/telemetry#how-to-opt-out
$env:DOTNET_CLI_TELEMETRY_OPTOUT = "true"

```
