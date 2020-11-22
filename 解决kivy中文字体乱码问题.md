## 在 Window 10 中 kivy 正常显示中文的方法


网络搜索你想要显示的字体并下载，如： “DroidSansFallback.ttf” ，以下的内容以本字体为例进行讲解

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

## Ubuntu18.04 20.04 环境下解决 kivy 中文显示问题

下载字体，并将字体复制到 main.py 文件同一目录下

```
import kivy
from kivy.app import App
from kivy.uix.button import Button

kivy.resources.resource_add_path('font/')
ft = kivy.resources.resource_find('DroidSansFallback.ttf')

class MyApp(App):
	def build(self):
		return Button(text='中文字体显示效果', font_size=50, font_name = ft)

MyApp().run()

```
