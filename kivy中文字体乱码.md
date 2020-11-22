Win 10 kivy 中文显示
下载上面的字体，解压缩后得到 “DroidSansFallback.ttf”
分别复制到C盘根目录（C:\DroidSansFallback.ttf）和代码目录（D:\Python\Kivy\DroidSansFallback.ttf）
我的代码放置目录是（D:\Python\Kivy\***）
添加如下代码

```
import kivy
···
kivy.resources.resource_add_path('font/')
ft = kivy.resources.resource_find('DroidSansFallback.ttf')
···
(text="我的世界!", font_name=ft)

```
