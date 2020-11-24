## 解决kivy文件显示乱码的问题

### 1.首先，下载在网上下载一个中文字体文件（如： DroidSansFallback.ttf ），放入文件根目录


### 2.创建一个python文件，如： main.py 代码如下

```
from kivy.app import App
from kivy.uix.widget import Widget
from kivy.lang import Builder

# These two lines are what opens the .kv file and uses the rules written within.
with open("chinese.kv", encoding='utf-8') as f:  # Note the name of the .kv
    # doesn't match the name of the App
    Builder.load_string(f.read())


class ChineseTest(Widget):
    pass


class ChineseTestApp(App):
    def build(self):
        return ChineseTest()


if __name__ == '__main__':
    ChineseTestApp().run()


```
### 3.创建一个kv文件，如： chinese.kv

```

<ChineseTest>:
    Label:
        size: self.texture_size
        font_size: 36
        font_name: "DroidSansFallback.ttf"
        text: "这是中文显示的效果"

```

### 整个文件结构为：

|- DroidSansFallback.ttf   #字体文件
|- main.py   # python主文件
|- chinese.kv  # kv文件 




