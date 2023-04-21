# VLC-For-Unity
这些是包含Unity对Android进行Ump格式播放的相关设置。

1.导入“UMP Pro Android iOS.unitypackage”出现
“Assets\UniversalMediaPlayer\Scripts\Sources\UMPSettings.cs(354,39): error CS1069: The type name 'Registry' could not be found in the namespace 'Microsoft.Win32'. This type has been forwarded to assembly 'Microsoft.Win32.Registry, Version=4.1.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a' Consider adding a reference to that assembly.”![image](https://user-images.githubusercontent.com/127721528/233581215-a4ba8e57-063c-4f37-97e0-569e5a17d337.png)
的错误。解决方法为“Project Settings->Player->Other Settings->Configuration->Api Compatibillity Level0”设置为“.net Framework”。
2.请采用默认路径安装VLC，及路径为C:\Program Files (x86)\VideoLAN\VLC。对Prefernces->Ump->Extemai/installed VLC libraries path进行检查。如果还是不可用，请用旧版本VLC安装，本次采用http://get.videolan.org/vlc/3.0.6/win64/vlc-3.0.6-win64.exe
3.![image](https://user-images.githubusercontent.com/127721528/233580020-c72910e2-dd72-4ee7-97a5-f765531cc27d.png)
对Universal Media Player进行设置为安卓，Player Type为LibVLC；
4.![image](https://user-images.githubusercontent.com/127721528/233580567-06f5c3a5-1924-4cf9-a0d3-3b141e464308.png)
打包时设置Other Setting中的AutoGraphics API取消勾选，Graphics ApIs设置OpenGLE33，不要Vulkan API。
