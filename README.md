Clear-Host
Write-Host @"
░██████╗░░██╗░██   ██╗░███████╗░████████╗░
░██╔══██╗░██║░██   ██║░██╔════╝░██    ██║░
░██████╔╝░██║░██   ██║░█████╗░░░████████║░
░██╔══██╗░██║░██   ██║░██╔══╝░░░██    ██║░
░██║░░██║░██║░░█████╔╝░███████╗░██    ██║░
░░╚╝░░╚╝░░╚╝░░░╚════╝░░╚══════╝░╚═══════╝░ 
"@ -ForegroundColor Cyan

Write-Host "Made by Rivea / Maverius for Your Sweetie`n"


$AppSwitchedPath = "HKCU:\Software\Microsoft\Windows\CurrentVersion\Explorer\FeatureUsage\AppSwitched"

Get-ItemProperty -Path $AppSwitchedPath |
    findstr /i /C:":\" |
    Sort-Object LastWriteTime |
    Out-GridView -PassThru -Title 'Appswitch Script by Gothic Girl lover'
