## 1. tsc -v 报错

```
tsc : 无法加载文件 C:\Users\Think\AppData\Roaming\npm\tsc.ps1，因为在此系统上禁止运行脚本。
```

以管理员身份运行 Windows PowerShell

```
 set-ExecutionPolicy RemoteSigned
 y
```

