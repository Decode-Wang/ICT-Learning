## Python数据分析IDE

Python统一安装如下的数据分析库[Anaconda](https://www.anaconda.com/)，在IDE上选择[PyCharm](https://www.jetbrains.com/pycharm/download/?section=windows)，在数据处理方面，统一采用pandas库，鉴于pandas需要一定的简单代码量，可以尝试采用图形化界面进行数据分析。D-tale是一款功能强大的基于pandas和python的具备GUI可视化界面的开源工具，操作就和Excel一样简单；当然类似的工具还有pandas-GUI等，本次学习D-tale.[github链接](https://github.com/man-group/dtale)

[pandas GUI 神器 D-Tale，可视化操作自动转代码！ - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/432832785)

`D-Tale`支持多种文件格式，包括`CSV`、`TSV`、`XLS`、`XLSX`。它是一个以`Flask` 为后端，`React` 作为前端构建的，通过`pip`安装即可。

```python3
pip install dtale
```

两种启动 D-Tale 的方式： - 将DataFrame对象传递给 D-Tale 函数，在 Jupyter 单元中实例化 GUI。 - 不导入DataFrame对象的情况下初始化 D-Tale，显示为一个带有 GUI 的交互菜单来加载数据并提供各种其他选项。

为了更好地演示，这里选择第二种，可以通过GUI界面的方式直接选择csv等文件，方便快捷，免去python代码写作过程，通过下述简单直接的方式来进行数据表格的操作。

```python3
import dtale
dtale.show()
```

如果上述的存在bug，或者认为csv文件太大，可以尝试直接采用pandas读取，然后作为df格式导入到dtale中，可以尝试如下命令，这样速度效率更快（dtale的文件导入采用web方式，速率低）：

```python3
import pandas as pd
import dtale
df=pd.read_csv(r'xxx')
d=dtale.show(df)
d.open_browser()
```

详细的指南参考：[Pandas可视化数据分析工具D-Tale详解 | 数字旗手 (qixinbo.info)](https://www.qixinbo.info/2022/12/17/dtale/)

