## 在 Window 10 中 kivy 正常显示中文的方法


下载上面的字体，解压缩后得到 “DroidSansFallback.ttf”

### 分别复制到C盘根目录和代码目录中

系统根目录：（C:\DroidSansFallback.ttf）

代码目录： （D:\Python\Kivy\DroidSansFallback.ttf）

添加如下代码

```
import kivy
···
kivy.resources.resource_add_path('font/')
ft = kivy.resources.resource_find('DroidSansFallback.ttf')
···
(text="中文字体显示效果", font_name=ft)

```
加入到文件中的样子

```
import kivy
from kivy.app import App
from kivy.uix.button import Button
#  设置字体
kivy.resources.resource_add_path('font/')
ft = kivy.resources.resource_find('DroidSansFallback.ttf')

class EpicApp(App):
    def build(self):
        return Label(text="中文字体显示效果 Hey there!", font_size=30, font_name=ft)

if __name__ == '__main__':
    EpicApp().run()
```
