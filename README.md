# 课程-计算机视觉-传统
更新中～～～


已更新：
- 01-图像基础知识
- 02-图像基本处理
- 03-图像分割（未完成）



# 导出 pdf
## 方法1：pandoc
转成 pdf，想给代码块添加方框，一只没有成功。但是代码块有明显的高亮并且字体格式不一样。
```commandline
pandoc 图像基础知识.ipynb --pdf-engine=xelatex --template=default-template.tex -o 图像基础知识.pdf
```
这里使用的引擎是 xelatex，并且要设置模版 `default-template.tex`。


## 方法2：nbconvert
```commandline
jupyter nbconvert --to webpdf 图像基础知识.ipynb --allow-chromium-download
```

这里需要注意的是，markdown 里面载入的图片可能会无法导出，需要使用这种方式加载图片：

```python
from IPython.display import display, Image
display(Image(filename='path_to_image.png'))
```

我估计如果把图片的地址写成绝对地址可以解决这个不现实markdown图片的问题，但是我没有实验。