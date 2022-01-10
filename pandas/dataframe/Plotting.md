- [**==DataFrame.plot(args,kwargs)==**](#dataframeplotargskwargs)
    - [制作Series或dataframe的绘图。使用 plotting.backend 选项指定的后端。默认情况下使用 matplotlib](#制作series或dataframe的绘图使用-plottingbackend-选项指定的后端默认情况下使用-matplotlib)
  - [参数设置：](#参数设置)
- [官网](#官网)
- [==**DataFrame.plot.**area==**(**x=None**,** *y=None***,** ***kwargs***)](#dataframeplotareaxnone-ynone-kwargs)
    - [绘制一个堆积的区域图。区域图直观地显示定量数据。此函数包装 matplotlib 区域函数。](#绘制一个堆积的区域图区域图直观地显示定量数据此函数包装-matplotlib-区域函数)
  - [参数设置：](#参数设置-1)
- [官网](#官网-1)
- [==**DataFrame.plot.**bar==**(**x=None**,** *y=None***,** ***kwargs***)](#dataframeplotbarxnone-ynone-kwargs)
    - [垂直条形图。条形图是用长度与它们所表示的值成正比的矩形条形图来表示范畴数据的图。条形图显示了离散类别之间的比较。图表的一个轴显示正在比较的特定类别，另一个轴代表一个测量值。](#垂直条形图条形图是用长度与它们所表示的值成正比的矩形条形图来表示范畴数据的图条形图显示了离散类别之间的比较图表的一个轴显示正在比较的特定类别另一个轴代表一个测量值)
  - [参数设置：](#参数设置-2)
- [官网](#官网-2)
- [==**DataFrame.plot.**barh==**(**x=None**,** *y=None***,** ***kwargs***)](#dataframeplotbarhxnone-ynone-kwargs)
    - [制作一个水平条形图。水平条形图是用长度与它们所代表的值成正比的矩形条来表示定量数据的图。条形图显示了离散类别之间的比较。图表的一个轴显示正在比较的特定类别，另一个轴代表一个测量值。](#制作一个水平条形图水平条形图是用长度与它们所代表的值成正比的矩形条来表示定量数据的图条形图显示了离散类别之间的比较图表的一个轴显示正在比较的特定类别另一个轴代表一个测量值)
  - [参数与上文一致](#参数与上文一致)
- [官网](#官网-3)
- [==**DataFrame.plot.**box==**(**by=None**,** ***kwargs***)](#dataframeplotboxbynone-kwargs)
    - [为 DataFrame 列绘制一个箱线图。盒子图是一种通过四分位数以图形方式描绘数值数据组的方法。盒子从数据的 q1延伸到 q3四分位数值，在中位数(Q2)上有一条直线。晶须从盒子的边缘延伸出来，显示数据的范围。晶须的位置默认设置为1.5 * IQR (IQR = Q3-Q1) ，从盒子的边缘开始。异常点是指那些超过胡须末端的点。更多详细信息请参阅维基百科的  boxplot 条目。使用此图表时要考虑的一点是，盒子和胡须可以重叠，这在绘制小数据集时非常常见。](#为-dataframe-列绘制一个箱线图盒子图是一种通过四分位数以图形方式描绘数值数据组的方法盒子从数据的-q1延伸到-q3四分位数值在中位数q2上有一条直线晶须从盒子的边缘延伸出来显示数据的范围晶须的位置默认设置为15--iqr-iqr--q3-q1-从盒子的边缘开始异常点是指那些超过胡须末端的点更多详细信息请参阅维基百科的--boxplot-条目使用此图表时要考虑的一点是盒子和胡须可以重叠这在绘制小数据集时非常常见)
  - [参数设置：](#参数设置-3)
- [==**DataFrame.plot.**density==**(**bw_method=None**,** *ind=None***,** ***kwargs***)](#dataframeplotdensitybw_methodnone-indnone-kwargs)
    - [利用高斯核生成核密度估计图。在统计学中，核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数。该函数采用高斯核函数，包括自动带宽确定。](#利用高斯核生成核密度估计图在统计学中核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数该函数采用高斯核函数包括自动带宽确定)
  - [参数设置：](#参数设置-4)
- [官网](#官网-4)
- [==**DataFrame.plot.**hexbin==**(**x**,** *y***,** *C=None***,** *reduce_C_function=None***,** *gridsize=None***,** ***kwargs***)](#dataframeplothexbinx-y-cnone-reduce_c_functionnone-gridsizenone-kwargs)
    - [生成一个六边形的结点图。生成一个 x 和 y 的六角形的边缘图。如果 c 是 None (默认值) ，这是一个直方图，显示观察值出现的次数(x [ i ] ，y [ i ])。如果指定了 c，则指定给定坐标(x [ i ] ，y [ i ])处的值。这些值为每个六边形容器积累，然后根据 reduce _ c _ 函数减少，默认情况下具有 NumPy 的平均值函数(NumPy.mean ()))。(如果指定了 c，它也必须是与 x 和 y 长度相同的1-d 序列，或者是列标签。)](#生成一个六边形的结点图生成一个-x-和-y-的六角形的边缘图如果-c-是-none-默认值-这是一个直方图显示观察值出现的次数x--i--y--i-如果指定了-c则指定给定坐标x--i--y--i-处的值这些值为每个六边形容器积累然后根据-reduce-_-c-_-函数减少默认情况下具有-numpy-的平均值函数numpymean-如果指定了-c它也必须是与-x-和-y-长度相同的1-d-序列或者是列标签)
  - [参数设置：](#参数设置-5)
- [官网](#官网-5)
- [==**DataFrame.plot.**hist==**(**by=None**,** *bins=10***,** ***kwargs***)](#dataframeplothistbynone-bins10-kwargs)
    - [为 DataFrame 的列绘制一个直方图。直方图是数据分布的表示。这个函数将 DataFrame 中所有给定系列的值分组到箱子中，并在一个 matplotlib.axes 中绘制所有箱子。轴线。当 DataFrame 系列处于类似的规模时，这是非常有用的。](#为-dataframe-的列绘制一个直方图直方图是数据分布的表示这个函数将-dataframe-中所有给定系列的值分组到箱子中并在一个-matplotlibaxes-中绘制所有箱子轴线当-dataframe-系列处于类似的规模时这是非常有用的)
  - [参数设置：](#参数设置-6)
- [官网](#官网-6)
- [==**DataFrame.plot.**kde==**(**bw_method=None**,** *ind=None***,** ***kwargs***)](#dataframeplotkdebw_methodnone-indnone-kwargs)
    - [利用高斯核生成核密度估计图。在统计学中， kernel density estimation 核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数。该函数采用高斯核函数，包括自动带宽确定。](#利用高斯核生成核密度估计图在统计学中-kernel-density-estimation-核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数该函数采用高斯核函数包括自动带宽确定)
  - [参数设置：](#参数设置-7)
- [官网](#官网-7)
- [==**DataFrame.plot.**line==**(**x=None**,** *y=None***,** ***kwargs***)](#dataframeplotlinexnone-ynone-kwargs)
    - [绘制系列或dataframe作为行。此函数可用于使用DataFrame的值作为坐标绘制行。](#绘制系列或dataframe作为行此函数可用于使用dataframe的值作为坐标绘制行)
  - [参数和 DataFrame.plot.bar 一致](#参数和-dataframeplotbar-一致)
- [官网](#官网-8)
- [==**DataFrame.plot.**pie==**(******kwargs**)](#dataframeplotpiekwargs)
    - [生成一个饼图。饼图是列中数值数据的比例代表制。此函数为指定列包装 matplotlib.pyplot.pie ()。如果没有传递列引用，并且子图形 = True，则为每个数值列分别绘制饼图。](#生成一个饼图饼图是列中数值数据的比例代表制此函数为指定列包装-matplotlibpyplotpie-如果没有传递列引用并且子图形--true则为每个数值列分别绘制饼图)
  - [参数设置：](#参数设置-8)
- [官网](#官网-9)
- [==**DataFrame.plot.**scatter==**(**x**,** *y***,** *s=None***,** *c=None***,** ***kwargs***)](#dataframeplotscatterx-y-snone-cnone-kwargs)
    - [创建一个散点图与不同的标记点大小和颜色。每个点的坐标由两个数据框列定义，填充的圆用于表示每个点。这种图对于观察两个变量之间的复杂关系是有用的。例如，点可以是自然的二维坐标，比如地图中的经纬度，或者，一般来说，任何一对可以相互绘制的度量。](#创建一个散点图与不同的标记点大小和颜色每个点的坐标由两个数据框列定义填充的圆用于表示每个点这种图对于观察两个变量之间的复杂关系是有用的例如点可以是自然的二维坐标比如地图中的经纬度或者一般来说任何一对可以相互绘制的度量)
  - [参数设置：](#参数设置-9)
- [官网](#官网-10)
- [==**DataFrame.**boxplot==**(**column=None**,** *by=None***,** *ax=None***,** *fontsize=None***,** *rot=0***,** *grid=True***,** *figsize=None***,** *layout=None***,** *return_type=None***,** *backend=None***,** ***kwargs***)](#dataframeboxplotcolumnnone-bynone-axnone-fontsizenone-rot0-gridtrue-figsizenone-layoutnone-return_typenone-backendnone-kwargs)
    - [从Dataframe列中制作一个盒子绘图。从DataFrame列中制作一个盒子和晶须绘图，可选地由其他一些列分组。盒绘图是通过它们的四分位数图形描绘数值数据组的方法。该框从Q1到Q3四分位数的数据值延伸，中位数（Q2）有一条线。晶须从框的边缘延伸以显示数据的范围。默认情况下，它们不会从框的边缘扩展到1.5 * IQR（IQR = Q3 - Q1），在该间隔内的最远数据点结束。异常值被绘制为单独的点。有关详细信息，请参阅Wikipedia for  boxplot的条目。](#从dataframe列中制作一个盒子绘图从dataframe列中制作一个盒子和晶须绘图可选地由其他一些列分组盒绘图是通过它们的四分位数图形描绘数值数据组的方法该框从q1到q3四分位数的数据值延伸中位数q2有一条线晶须从框的边缘延伸以显示数据的范围默认情况下它们不会从框的边缘扩展到15--iqriqr--q3---q1在该间隔内的最远数据点结束异常值被绘制为单独的点有关详细信息请参阅wikipedia-for--boxplot的条目)
  - [参数设置：](#参数设置-10)
- [官网](#官网-11)
- [==**DataFrame.**hist==**(**column=None**,** *by=None***,** *grid=True***,** *xlabelsize=None***,** *xrot=None***,** *ylabelsize=None***,** *yrot=None***,** *ax=None***,** *sharex=False***,** *sharey=False***,** *figsize=None***,** *layout=None***,** *bins=10***,** *backend=None***,** *legend=False***,** ***kwargs***)](#dataframehistcolumnnone-bynone-gridtrue-xlabelsizenone-xrotnone-ylabelsizenone-yrotnone-axnone-sharexfalse-shareyfalse-figsizenone-layoutnone-bins10-backendnone-legendfalse-kwargs)
    - [为 DataFrame 的列制作一个直方图。直方图是数据分布的表示。这个函数对 DataFrame 中的每个序列调用 matplotlib.pyplot.hist () ，结果是每列有一个直方图。](#为-dataframe-的列制作一个直方图直方图是数据分布的表示这个函数对-dataframe-中的每个序列调用-matplotlibpyplothist--结果是每列有一个直方图)
  - [参数设置：](#参数设置-11)
  - [***data***：**DataFrame**](#datadataframe)
- [官网](#官网-12)

#### **==DataFrame.plot(args,kwargs)==**

###### 制作Series或dataframe的绘图。使用 plotting.backend 选项指定的后端。默认情况下使用 matplotlib

##### 参数设置：

​	***data*：Series or DataFrame**

​		调用方法的对象。

​	***x* : label or position, default None**

​		只有当数据是 DataFrame 时才使用。

​	***y*：label, position or list of label, positions, default None**

​		允许绘制一列与另一列之间的图形。只有当数据是 DataFrame 时才使用。

​	***kind*：str**

​		产生plot的类型：

​			‘line’: 折线图(默认)

​			‘bar’:条形图

​			‘barh’:横向条形图

​			‘hist’:柱状图

​			‘box’:箱线图

​			‘kde’:核密度估计图

​			‘density’:same as ‘kde’

​			‘area’:区域图

​			‘pie’:饼图

​			‘scatter’:散点图(DataFrame only)

​			‘hexbin’:蜂巢图(DataFrame only)

​	***ax*:matplotlib axes object, default None**

​		目前图的轴。

​	***subplots*:bool, default False**

​		为每一列制作单独的次要图。

​	***sharex*:bool, default True if ax is None else False**

​		如果传入 ax，则默认为 True; 如果传入 ax，则默认为 True; 如果传入 ax 和 sharex = True，则要注意，同时传入 ax 和 sharex = True 将改变图形中所有轴的所有 x 轴标记。

​	***sharey*:bool, default False**

​		在 case subplot = True 中，共享 y 轴并将一些 y 轴标签设置为 invisible。

​	***layout*:tuple, optional**

​		(行，列)用于子图的布局。

​	***figsize*:a tuple (width, height) in inches**

​		图形对象的大小。

​	***use_index*:bool, default True**

​		使用索引作为 x 轴的刻度。

​	***title*:str or list**

​		plot使用的标题。如果传递了字符串，则在图的顶部打印该字符串。如果传递了一个列表，并且子图为 True，则在相应的子图之上打印列表中的每个项。

​	***grid*:bool, default None (matlab style default)**

​		轴线网格线。

​	***legend*:bool or {‘reverse’}**

​		将图例放在轴的次要图上。

​	***style*:list or dict**

​		每列的 matplotlib 行样式。

​	***logx*:bool or ‘sym’, default False**

​		在 x 轴上使用日志缩放或对称缩放. . versionchanged: : 0.25.0

​	***logy*:bool or ‘sym’ default False**

​		在 y 轴上使用日志缩放或对称缩放. . versionchanged: : 0.25.0

​	***loglog*:bool or ‘sym’, default False**

​		在 x 轴和 y 轴上使用日志缩放或对称缩放

​	***xticks*:sequence**

​		用于 xticks 的值。

​	***yticks*:sequence**

​		要用于 yticks 的值。

​	***xlim***:**2-tuple/list**

​		设置当前轴的 x 限制。

​	***ylim***:**2-tuple/list**

​		设置当前轴的 y 限值。

​	***xlabel***:**label, optional**

​		要用于 x 轴上的 xlabel 的名称。Default 使用索引名称作为 xlabel，或者使用平面图的 x 列名称。

​	***ylabel***:**label, optional**

​		要用于 y 轴上的 ylabel 的名称。默认情况下不显示 ylabel，或者平面图的 y 列名称。

​	***rot***:**int, default None**

​		旋转刻度(xticks 表示垂直，yticks 表示水平地块)。

​	***fontsize***:**int, default None**

​		Xticks 和 yticks 的字体大小。

​	***colormap*:str or matplotlib colormap object, default None**

​		从中选择颜色。如果是字符串，从 matplotlib 加载同名的颜色映射。

​	***colorbar*:bool, optional**

​		如果为真，则绘图颜色条(仅适用于“散点”和“ hexbin”绘图)。

​	***position*:float**

​		为条形图布局指定相对比对。从0(左/底端)到1(右/顶端)。默认值为0.5(中间)。

​	***table*:bool, Series or DataFrame, default False**

​		如果为 True，则使用 DataFrame 中的数据绘制一个表，数据将被转换以满足 matplotlib 的默认布局。如果传递了 Series 或 DataFrame，则使用传递的数据绘制表。

​	***yerr*:DataFrame, Series, array-like, dict and str**

​		有关详细信息，请参阅[Plotting with Error Bars](https://pandas.pydata.org/docs/user_guide/visualization.html#visualization-errorbars)

​	***xerr*:DataFrame, Series, array-like, dict and str**

​		相当于 yerr。

​	***stacked*:bool, default False in line and bar plots, and True in area plot**

​		如果为真，创建堆叠的plot。

​	***sort_columns*:bool, default False**

​		对列名进行排序以确定绘图顺序。

​	***secondary_y*:bool or sequence, default False**

​		是否在次要 y 轴上绘制列表/元组，该列在次要 y 轴上绘制。

​	***mark_right*:bool, default True**

​		当使用辅助 _y 轴时，在图例中自动用“(右)”标记列标签。

​	***include_bool*:bool, default is False**

​		如果为真，则可以绘制布尔值。

​	***backend*:str, default None**

​		使用后端而不是选项 plotting.Backend 中指定的后端。例如 matplotlib。或者，要为整个会话指定 plotting.backend，请设置 pd.options.plotting.backend。

​	***\*kwargs**:传递给 matplotlib 绘图方法的选项。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html)

#### ==**DataFrame.plot.**area==**(**x=None**,** *y=None***,** ***kwargs***)

###### 绘制一个堆积的区域图。区域图直观地显示定量数据。此函数包装 matplotlib 区域函数。

##### 参数设置：

​	***x***：**label or position, optional**

​		X 轴的坐标。默认情况下使用索引。

​	***y***：**label or position, optional**

​		要绘制的列。默认情况下使用所有列。

​	***stacked*：bool, default True**

​		默认情况下堆叠区域图。设置为false以创建未堆叠的绘图。	

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.area.html)

#### ==**DataFrame.plot.**bar==**(**x=None**,** *y=None***,** ***kwargs***)

###### 垂直条形图。条形图是用长度与它们所表示的值成正比的矩形条形图来表示范畴数据的图。条形图显示了离散类别之间的比较。图表的一个轴显示正在比较的特定类别，另一个轴代表一个测量值。

##### 参数设置：

​	***x***：**label or position, optional**

​		允许绘制一列与另一列之间的图形。如果没有指定，则使用 DataFrame 的索引。

​	***y***：**label or position, optional**

​		允许绘制一列与另一列之间的图形。如果没有指定，则使用所有的数字列。		

​	***color***：**str, array-like, or dict, optional**

​		每个 DataFrame 列的颜色。可能的值是:

​				由名称、 RGB 或 RGBA 代码引用的单个颜色字符串,比如“ red”或者“ # a98d19”。

​				一个由名称、 RGB 或 RGBA 引用的颜色字符串序列，代码，递归地用于每个列。例如[’绿色’,’黄色’]每一栏的栏将填写绿色或黄色，交替。如果只有一列要绘制，则只使用颜色列表中的第一个颜色。

​				一个字典的形式{列名称颜色} ，所以每个列将有相应的颜色。例如，如果你的列被称为 a 和 b，那么传递{‘ a’: ‘ green’，‘ b’: ‘ red’}将把 a 列的栏设为绿色，把 b 列的栏设为红色。

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.bar.html)

#### ==**DataFrame.plot.**barh==**(**x=None**,** *y=None***,** ***kwargs***)

###### 制作一个水平条形图。水平条形图是用长度与它们所代表的值成正比的矩形条来表示定量数据的图。条形图显示了离散类别之间的比较。图表的一个轴显示正在比较的特定类别，另一个轴代表一个测量值。

##### 参数与上文一致

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.barh.html)

#### ==**DataFrame.plot.**box==**(**by=None**,** ***kwargs***)

###### 为 DataFrame 列绘制一个箱线图。盒子图是一种通过四分位数以图形方式描绘数值数据组的方法。盒子从数据的 q1延伸到 q3四分位数值，在中位数(Q2)上有一条直线。晶须从盒子的边缘延伸出来，显示数据的范围。晶须的位置默认设置为1.5 * IQR (IQR = Q3-Q1) ，从盒子的边缘开始。异常点是指那些超过胡须末端的点。更多详细信息请参阅维基百科的  [boxplot](https://en.wikipedia.org/wiki/Box_plot) 条目。使用此图表时要考虑的一点是，盒子和胡须可以重叠，这在绘制小数据集时非常常见。

##### 参数设置：

​	**by：str or sequence**

​		按照以下方式分组。

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### ==**DataFrame.plot.**density==**(**bw_method=None**,** *ind=None***,** ***kwargs***)

###### 利用高斯核生成核密度估计图。在统计学中，核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数。该函数采用高斯核函数，包括自动带宽确定。

##### 参数设置：

​	**bw_method：str, scalar or callable, optional**

​		用于计算估计器带宽的方法。这可以是“ scott”、“ silverman”、标量常量或可调用。如果没有(默认值) ，则使用‘ scott’。更多信息请参见 scipy.stats.gaussian _ kde。

​	**ind：NumPy array or int, optional**

​		估计 PDF 的评估点。如果没有(默认值) ，则使用1000个等间距点。如果 ind 是 NumPy 数组，则在传递的点计算 KDE。如果 ind 是一个整数，则使用等间距点的 ind 数。

​	***\*kwargs**：在 pandas.% (this-datatype) s.plot ()中记录了其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.density.html)

#### ==**DataFrame.plot.**hexbin==**(**x**,** *y***,** *C=None***,** *reduce_C_function=None***,** *gridsize=None***,** ***kwargs***)

###### 生成一个六边形的结点图。生成一个 x 和 y 的六角形的边缘图。如果 c 是 None (默认值) ，这是一个直方图，显示观察值出现的次数(x [ i ] ，y [ i ])。如果指定了 c，则指定给定坐标(x [ i ] ，y [ i ])处的值。这些值为每个六边形容器积累，然后根据 reduce _ c _ 函数减少，默认情况下具有 NumPy 的平均值函数(NumPy.mean ()))。(如果指定了 c，它也必须是与 x 和 y 长度相同的1-d 序列，或者是列标签。)

##### 参数设置：

​	***x***：**int or str**

​		X 点的列标签或位置。

​	***y***：**int or str**

​		y 点的列标签或位置。

​	***reduce_C_function***：**callable, default np.mean**

​		一个参数的函数，该参数将 bin 中的所有值减少为一个数字(例如 np.mean，np.max，np.sum，np.std)。

​	***gridsize***：**int or tuple of (int, int), default 100**

​		X 方向上六边形的数目。选择 y 方向相应数目的六边形时，六边形大致是正则的。或者，gridsize 可以是一个元组，其中两个元素指定 x 方向和 y 方向的六边形数目。

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.hexbin.html)

#### ==**DataFrame.plot.**hist==**(**by=None**,** *bins=10***,** ***kwargs***)

###### 为 DataFrame 的列绘制一个直方图。直方图是数据分布的表示。这个函数将 DataFrame 中所有给定系列的值分组到箱子中，并在一个 matplotlib.axes 中绘制所有箱子。轴线。当 DataFrame 系列处于类似的规模时，这是非常有用的。

##### 参数设置：

​	**by：str or sequence, optional**

​		按照以下方式分组。

​	**bins**：**int, default 10**

​		要使用的直方图箱数。

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.hist.html)

#### ==**DataFrame.plot.**kde==**(**bw_method=None**,** *ind=None***,** ***kwargs***)

###### 利用高斯核生成核密度估计图。在统计学中， [kernel density estimation](https://en.wikipedia.org/wiki/Kernel_density_estimation) 核密度估计是一种非参数的方法来估计一个随机变量的概率密度函数。该函数采用高斯核函数，包括自动带宽确定。

##### 参数设置：

​	**bw_method：str, scalar or callable, optional**

​		用于计算估计器带宽的方法。这可以是“ scott”、“ silverman”、标量常量或可调用。如果没有(默认值) ，则使用‘ scott’。更多信息请参见 [`scipy.stats.gaussian_kde`](https://docs.scipy.org/doc/scipy/reference/reference/generated/scipy.stats.gaussian_kde.html#scipy.stats.gaussian_kde) 

​	**ind：NumPy array or int, optional**

​		估计 PDF 的评估点。如果没有(默认值) ，则使用1000个等间距点。如果 ind 是 NumPy 数组，则在传递的点计算 KDE。如果 ind 是一个整数，则使用等间距点的 ind 数。

​	***\*kwargs**：在 pandas.% (this-datatype) s.plot ()中记录了其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.kde.html)

#### ==**DataFrame.plot.**line==**(**x=None**,** *y=None***,** ***kwargs***)

###### 绘制系列或dataframe作为行。此函数可用于使用DataFrame的值作为坐标绘制行。

##### 参数和 DataFrame.plot.bar 一致

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.line.html)

#### ==**DataFrame.plot.**pie==**(******kwargs**)

###### 生成一个饼图。饼图是列中数值数据的比例代表制。此函数为指定列包装 matplotlib.pyplot.pie ()。如果没有传递列引用，并且子图形 = True，则为每个数值列分别绘制饼图。

##### 参数设置：

​	**y：int or label, optional**

​		要绘制的列的标签或位置。如果没有提供，则必须传递 subplot = True 参数。

​	***\*kwargs**：其他关键字参数在 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.pie.html)

#### ==**DataFrame.plot.**scatter==**(**x**,** *y***,** *s=None***,** *c=None***,** ***kwargs***)

###### 创建一个散点图与不同的标记点大小和颜色。每个点的坐标由两个数据框列定义，填充的圆用于表示每个点。这种图对于观察两个变量之间的复杂关系是有用的。例如，点可以是自然的二维坐标，比如地图中的经纬度，或者，一般来说，任何一对可以相互绘制的度量。

##### 参数设置：

​	**x**：**int or str**

​		要用作每个点的水平坐标的列名或列位置。

​	**y**：**int or str**

​		要用作每个点的垂直坐标的列名或列位置。

​	**s**：**str, scalar or array-like, optional**

​		每个点的大小。可能的值是:

​			一个字符串，其中包含用于标记的大小的列的名称。

​			单个标量，因此所有点具有相同的大小。

​			一个标量序列，递归地用于每个点的大小。例如，当传递[2,14]时，所有的点大小可以选择为2或14。	

​	**c**：**str, int or array-like, optional**

​		每个点的颜色。可能的值是:

​			一个由名称、 RGB 或 RGBA 代码引用的单色字符串，例如“ red”或“ # a98d19”。

​			一个由名称、 RGB 或 RGB 代码引用的颜色字符串序列，它将递归地用于每个点的颜色。例如[’绿色’,’黄色’]所有点将填写绿色或黄色，交替。

​			一个列名或位置，其值将用于根据颜色映射为标记点着色。

​	***\*kwargs**：关键字参数传递到 [`DataFrame.plot()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot)

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.scatter.html)

#### ==**DataFrame.**boxplot==**(**column=None**,** *by=None***,** *ax=None***,** *fontsize=None***,** *rot=0***,** *grid=True***,** *figsize=None***,** *layout=None***,** *return_type=None***,** *backend=None***,** ***kwargs***)

###### 从Dataframe列中制作一个盒子绘图。从DataFrame列中制作一个盒子和晶须绘图，可选地由其他一些列分组。盒绘图是通过它们的四分位数图形描绘数值数据组的方法。该框从Q1到Q3四分位数的数据值延伸，中位数（Q2）有一条线。晶须从框的边缘延伸以显示数据的范围。默认情况下，它们不会从框的边缘扩展到1.5 * IQR（IQR = Q3 - Q1），在该间隔内的最远数据点结束。异常值被绘制为单独的点。有关详细信息，请参阅Wikipedia for  [boxplot](https://en.wikipedia.org/wiki/Box_plot)的条目。

##### 参数设置：

​	***column***：**str or list of str, optional**

​		列名或名称或向量列表。可以是 [`pandas.DataFrame.groupby()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html#pandas.DataFrame.groupby) 的任何有效输入。

​	***by***：**str or array-like, optional**

​		在[`pandas.DataFrame.groupby()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html#pandas.DataFrame.groupby)中，每个列的值到年将完成一个盒式绘图。

​	***ax*：object of class matplotlib.axes.Axes, optional**

​		将由箱线图使用的 matplotlib 轴。

​	***fontsize*：float or str**

​		刻度标签字体大小以点或字符串（例如，大）。

​	***rot*：int or float, default 0**

​		标签相对于屏幕坐标系的旋转角度(度)。

​	***grid*：bool, default True**

​		将此设置为true将显示网格。

​	***figsize*：A tuple (width, height) in inches**

​		要在 matplotlib 中创建的图形的大小。	

​	***layout*：tuple (rows, columns), optional**

​		例如，(3,5)将使用3列和5行显示子图，从左上角开始。		

​	***return_type*：{‘axes’, ‘dict’, ‘both’} or None, default ‘axes’**

​		返回的对象类型。默认是轴。

​			‘ axes’返回箱线图所绘制的 matplotlib 轴。

​			‘ dict’返回一个值为箱线图的 matplotlib 行的字典。

​			‘ both’返回一个带有轴和 dict 的命名 tuple。

​			当使用 by 进行分组时，将返回要返回 _ type 的 Series 映射列。

​			如果 return _ type 为 None，则返回形状与布局相同的轴的 NumPy 数组。

​	***backend*：str, default None**

​		使用后端而不是选项 plotting.Backend 中指定的后端。例如 matplotlib。或者，要为整个会话指定 plotting.backend，请设置 pd.options.plotting.backend。

​	***\*kwargs**：要传递给的所有其他绘图关键字参数在 [`matplotlib.pyplot.boxplot()`](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.boxplot.html#matplotlib.pyplot.boxplot).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.boxplot.html)

#### ==**DataFrame.**hist==**(**column=None**,** *by=None***,** *grid=True***,** *xlabelsize=None***,** *xrot=None***,** *ylabelsize=None***,** *yrot=None***,** *ax=None***,** *sharex=False***,** *sharey=False***,** *figsize=None***,** *layout=None***,** *bins=10***,** *backend=None***,** *legend=False***,** ***kwargs***)

###### 为 DataFrame 的列制作一个直方图。直方图是数据分布的表示。这个函数对 DataFrame 中的每个序列调用 matplotlib.pyplot.hist () ，结果是每列有一个直方图。

##### 参数设置：

##### 	***data***：**DataFrame**

​		pandas对象持有数据。

​	***column*：str or sequence, optional**

​		如果通过，将用于将数据限制为列的子集。

​	***by*：object, optional**

​		如果通过，则用于为单独的组形成直方图。

​	***grid*：bool, default True**

​		是否显示轴网格线。

​	***xlabelsize*：int, default None**

​		如果指定，则更改 x 轴标签大小。

​	***xrot*：float, default None**

​		旋转 x 轴标签。例如，90的值显示 x 标签顺时针旋转90度。	***ylabelsize*：int, default None**

​		如果指定，则更改 y 轴标签大小。

​	***yrot*：float, default None**

​		Y 轴标签的旋转。例如，90的值显示 y 标签顺时针旋转了90度。

​	***ax***：**Matplotlib axes object, default None**

​		绘制直方图的坐标轴。

​	***sharex***：**bool, default True if ax is None else False**

​		在 case subplot = True 中，共享 x 轴并设置一些 x 轴标签为 invisible; 如果 ax 为 None，则默认为 True; 如果传入 ax，则为 False。注意，同时传入 ax 和 sharex = True 将改变图中所有子图的所有 x 轴标签。

​	***sharey***：**bool, default False**

​		在 case subplot = True 中，共享 y 轴并将一些 y 轴标签设置为 invisible。

​	***figsize***：**tuple, optional**

​		要创建的图形的英寸大小。默认情况下使用 matplotlib.rcParams 中的值。

​	***layout***：**tuple, optional**

​		用于直方图布局的元组(行、列)。

​	***bins***：**int or sequence, default 10**

​		要使用的直方图箱数。如果给出了整数，则计算并返回BINS + 1 BIN边缘。如果箱子是序列，请给出bin边缘，包括第一箱和最后边缘的左边缘。在这种情况下，返回垃圾箱未修改。

​	***backend***：**str, default None**

​		使用后端而不是选项 plotting.Backend 中指定的后端。例如 matplotlib。或者，要为整个会话指定 plotting.backend，请设置 pd.options.plotting.backend。

​	***legend***：**bool, default False**

​		是否显示图例。

​	***\*kwargs**：要传递给 matplotlib.pyplot.hist ()的所有其他标绘关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.hist.html)

