## 禁用模块
```batch
::关闭快速启动
powercfg /h off
::禁用索引服务
sc stop WSearch
sc config WSearch start= disabled
::禁用诊断跟踪服务
sc stop DiagTrack
sc config DiagTrack start= disabled
::禁用诊断执行服务，服务主机诊断，系统主机诊断
sc stop diagsvc
sc config diagsvc start= disabled
sc stop WdiServiceHost
sc config WdiServiceHost start= disabled
sc stop WdiSystemHost
sc config WdiSystemHost start= disabled
::禁用错误报告
sc stop WerSvc
sc config WerSvc start= disabled
::禁用脱机文件
sc stop CscService
sc config CscService start= disabled
::删除IE浏览器
Dism /Online /Disable-Feature /FeatureName:Internet-Explorer-Optional-amd64 /Remove /NoRestart
::删除媒体功能和Windows Media Player
Dism /Online /Disable-Feature /FeatureName:MediaPlayback /Remove /NoRestart
Dism /Online /Disable-Feature /FeatureName:WindowsMediaPlayer /Remove /NoRestart
pause
```

## 激活系统
产品密钥：[通用批量许可证密钥](https://docs.microsoft.com/zh-cn/windows-server/get-started/kms-client-activation-keys#generic-volume-license-keys-gvlk)  
win10/11专业版KMS激活
```batch
slmgr /ckms

slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX

slmgr /skms kms.03k.org

slmgr /ato
```

## 任意更改系统更新暂停的时间
```batch
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" /v FlightSettingsMaxPauseDays /t reg_dword /d 5000 /f
```
