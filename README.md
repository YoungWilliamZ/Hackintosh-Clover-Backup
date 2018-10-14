# Hackintosh-Clover-Backup

系统：10.13.6
机型：HP 暗影精灵2
CPU: i5 6300HQ
GPU: HD530

基本完美， 能调节亮度，音量

***注意***：X86PlatformPluginInjector.kext 这里只适用于 `i5 6300HQ`, 其他的 CPU 请自行查找相关教程完善

# 将 LE 文件中的 *.kext 复制到 /L/E/ 下

1. `cd` 到 LE 文件夹
2.
``` bash
sudo cp -R *.kext /Library/Extensions
```
3. sudo kextcache -i /

4. 结果：
``` bash
Kext with invalid signatured (-67030) allowed: <OSKext 0x7f8397fce530 [0x7fff8f9e2af0]> { URL = "X86PlatformPluginInjector.kext/ -- file:///Library/Extensions/", ID = "com.apple.driver.X86PlatformPlugin" }
Kext with invalid signatured (-67062) allowed: <OSKext 0x7f8395604a70 [0x7fff8f9e2af0]> { URL = "AppleBacklightInjector.kext/ -- file:///Library/Extensions/", ID = "org.rehabman.injector.AppleBacklightInjector" }
KernelCache ID: 94369CF39219C592853A1833EAFB816A
Kext with invalid signatured (-67062) allowed: <OSKext 0x7fa1af70a1b0 [0x7fff8f9e2af0]> { URL = "AppleBacklightInjector.kext/ -- file:///Library/Extensions/", ID = "org.rehabman.injector.AppleBacklightInjector" }
Kext with invalid signatured (-67030) allowed: <OSKext 0x7fa1b19fb790 [0x7fff8f9e2af0]> { URL = "X86PlatformPluginInjector.kext/ -- file:///Library/Extensions/", ID = "com.apple.driver.X86PlatformPlugin" }
```


# 参考：
1. https://www.xsit.top/2018/08/29/9.html
这个基本完美，但打开备忘录会卡
2. https://github.com/sqlsec/clover/tree/master/%E7%AC%94%E8%AE%B0%E6%9C%AC/%E6%83%A0%E6%99%AE/%E6%83%A0%E6%99%AE%E5%85%89%E5%BD%B1%E7%B2%BE%E7%81%B52%2Bi5-6300HQ%2B10.13/CLOVER
这个没有亮度调节
3. http://www.sqlsec.com/2018/09/hidpi.html
开启 HiDPI，放大一点不伤眼