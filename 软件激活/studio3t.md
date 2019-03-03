### Studio 3T 破解教程

1、创建文件studio3t.bat

```
@echo off
ECHO 重置Studio 3T的使用日期......
FOR /f "tokens=1,2,* " %%i IN ('reg query "HKEY_CURRENT_USER\Software\JavaSoft\Prefs\3t\mongochef\enterprise" ^| find /V "installation" ^| find /V "HKEY"') DO ECHO yes | reg add "HKEY_CURRENT_USER\Software\JavaSoft\Prefs\3t\mongochef\enterprise" /v %%i /t REG_SZ /d ""
ECHO 重置完成, 按任意键退出......
pause>nul
exit

```

2、将文件studio3t.bat文件移动到如下路径中
```commandline
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp
```
