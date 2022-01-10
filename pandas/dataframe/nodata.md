- [**==DataFrame.count==**(axis=0, level=None, numeric_only=False)](#dataframecountaxis0-levelnone-numeric_onlyfalse)
    - [对每个列或行计数非 na 单元格。值None，NaN，NaT和可选的numpy.inf（取决于pandas.options.mode.use_inf_as_na）被视为NA。](#对每个列或行计数非-na-单元格值nonenannat和可选的numpyinf取决于pandasoptionsmodeuse_inf_as_na被视为na)
  - [参数设置：](#参数设置)
- [官网](#官网)
- [**==DataFrame.dropna==**(axis=0, how='any', thresh=None, subset=None, inplace=False)](#dataframedropnaaxis0-howany-threshnone-subsetnone-inplacefalse)
  - [删除缺失的值。](#删除缺失的值)
  - [参数设置：](#参数设置-1)
- [官网](#官网-1)
- [**==DataFrame.backfill\bfill\ffill\pad==**(axis=None, inplace=False, limit=None, downcast=None)](#dataframebackfillbfillffillpadaxisnone-inplacefalse-limitnone-downcastnone)
    - [与DataFrame.fillna() 设置method='bfill\ffill'相同](#与dataframefillna-设置methodbfillffill相同)
- [官网](#官网-2)
- [**==DataFrame.fillna==**(value=None, method=None, axis=None, inplace=False, limit=None, downcast=None)](#dataframefillnavaluenone-methodnone-axisnone-inplacefalse-limitnone-downcastnone)
    - [使用指定的方法填充NA/NaN值。](#使用指定的方法填充nanan值)
  - [参数设置：](#参数设置-2)
- [官网](#官网-3)
- [**==DataFrame.interpolate==**(method='linear', axis=0, limit=None, inplace=False, limit_direction=None, limit_area=None, downcast=None, **kwargs)](#dataframeinterpolatemethodlinear-axis0-limitnone-inplacefalse-limit_directionnone-limit_areanone-downcastnone-kwargs)
    - [根据不同的方法插值。请注意，只有method='linear'具有MultiIndex的DataFrame/Series支持。‘krogh’, ‘piecewise_polynomial’, ‘spline’, ‘pchip’ 和 ‘akima’ 方法是类似名称的相应SciPy实现的包装。这些使用索引的实际数值。有关其行为的更多信息，请参见 SciPy文档 和SciPy教程。](#根据不同的方法插值请注意只有methodlinear具有multiindex的dataframeseries支持krogh-piecewise_polynomial-spline-pchip-和-akima-方法是类似名称的相应scipy实现的包装这些使用索引的实际数值有关其行为的更多信息请参见-scipy文档-和scipy教程)
  - [参数设置：](#参数设置-3)
- [官网](#官网-4)
- [**==DataFrame.isna\isnull==**()](#dataframeisnaisnull)
    - [检测缺失值。返回一个布尔值相同大小的对象，指示值是否为NA。NA值（例如,None或numpy.NaN）被映射为True值。其他所有内容都映射为False值。诸如空字符串之类的字符''或numpy.inf不被视为NA值的字符（除非您设置）。pandas.options.mode.use_inf_as_na = True](#检测缺失值返回一个布尔值相同大小的对象指示值是否为nana值例如none或numpynan被映射为true值其他所有内容都映射为false值诸如空字符串之类的字符或numpyinf不被视为na值的字符除非您设置pandasoptionsmodeuse_inf_as_na--true)
- [官网](#官网-5)
- [**==DataFrame.notna\notnull==**()](#dataframenotnanotnull)
    - [检测现有（非缺失）值。返回一个布尔值相同大小的对象，指示值是否不是NA。非缺失值将映射为True。诸如空字符串之类的字符''或numpy.inf不视为NA值的字符（除非设置pandas.options.mode.use_inf_as_na = True) 。NA值(例如，None或numpy.NaN)被映射为False值。](#检测现有非缺失值返回一个布尔值相同大小的对象指示值是否不是na非缺失值将映射为true诸如空字符串之类的字符或numpyinf不视为na值的字符除非设置pandasoptionsmodeuse_inf_as_na--true-na值例如none或numpynan被映射为false值)
- [官网](#官网-6)

#### **==DataFrame.count==**(axis=0, level=None, numeric_only=False)

###### 对每个列或行计数非 na 单元格。值None，NaN，NaT和可选的numpy.inf（取决于pandas.options.mode.use_inf_as_na）被视为NA。

##### 参数设置：

​	**axis**：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		如果为每列生成0或'index'计数。如果为每行生成1或'columns'计数

​	***leve***：**int or str, optional**

​		如果轴是MultiIndex（分层），则沿特定级别计数，折叠到DataFrame中。一个str指定级别名称。

​	***numeric_only***：**bool, default False**

​		仅包含float，int或boolean数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.count.html)

#### **==DataFrame.dropna==**(axis=0, how='any', thresh=None, subset=None, inplace=False)

##### 删除缺失的值。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		确定是否删除包含缺失值的行或列。0或'index'：删除包含缺失值的行。1或“columns”：删除包含缺失值的列。

​	***how***：**{‘any’, ‘all’}, default ‘any’**

​		当我们有至少一个NA或全部NA时，确定是否从DataFrame中删除行或列。

​			'any'：如果存在任何NA值，则删除该行或列。

​			'all'：如果所有值均为NA，则删除该行或列。

​	***thresh***：**int, optional**

​		需要许多非NA值。

​	***subset***：**array-like, optional**

​		要考虑的其他轴上的标签，例如，如果要删除行，这些标签将是要包括的列的列表。

​	***inplace***：**bool, default False**

​		如果为True，则执行就地操作并返回None。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html)

#### **==DataFrame.backfill\bfill\ffill\pad==**(axis=None, inplace=False, limit=None, downcast=None)

###### 与DataFrame.fillna() 设置method='bfill\ffill'相同

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.backfill.html)

#### **==DataFrame.fillna==**(value=None, method=None, axis=None, inplace=False, limit=None, downcast=None)

###### 使用指定的方法填充NA/NaN值。

##### 参数设置：

​	***value***：**scalar, dict, Series, or DataFrame**

​		用于填充孔的值（例如0），或者是dict / Series / DataFrame的值，该值指定用于每个索引（对于Series）或列（对于DataFrame）使用哪个值。不在dict / Series / DataFrame中的值将不被填充。该值不能是列表(list)。

​	***method***： **{‘backfill’, ‘bfill’, ‘pad’, ‘ffill’, None}, default None**

​		用于填充reindexed Serie的填充孔的方法

​			pad / ffill：传播上一个有效观测结果到下一个有效观测结果

​			backfill / bfill：用下一个有效的观察来填补空白。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}**

​		填充缺失值所沿的轴。

​	***inplace***：**bool, default False**

​		如果为True，则就地填充。注意：这将修改此对象上的任何其他视图（例如，DataFrame中列的无副本切片）。

​	***limit***：**int, default None**

​		如果指定了method，则这是要向前/向后填充的连续NaN值的最大数量。换句话说，如果存在连续的NaN数量大于此数量的缺口，它将仅被部分填充。如果未指定method，则这是将填写NaN的整个轴上的最大条目数。如果不为None，则必须大于0。

​	***downcast***：**dict, default is None**

​		item-> dtype的字典，如果可能的话，将向下转换，或者是字符串“infer”，它将尝试向下转换为适当的相等类型（例如，如果可能，则从float64到int64）。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.fillna.html)

#### **==DataFrame.interpolate==**(method='linear', axis=0, limit=None, inplace=False, limit_direction=None, limit_area=None, downcast=None, **kwargs)

###### 根据不同的方法插值。请注意，只有method='linear'具有MultiIndex的DataFrame/Series支持。‘krogh’, ‘piecewise_polynomial’, ‘spline’, ‘pchip’ 和 ‘akima’ 方法是类似名称的相应SciPy实现的包装。这些使用索引的实际数值。有关其行为的更多信息，请参见 SciPy文档 和SciPy教程。

##### 参数设置：

​	***method*** ：**str, default ‘linear’**

​		使用插值技术。其中之一:

​			'linear': 忽略索引并将值视为等间距。这是多索引支持的唯一方法。

​			'time': 处理每日和更高分辨率的数据，插值给定的间隔长度

​			‘index’, ‘values’: 使用索引的实际数值。

​			'pad'：使用现有值填写NaN。

​			‘nearest’, ‘zero’, ‘slinear’, ‘quadratic’, ‘cubic’, ‘spline’, ‘barycentric’, ‘polynomial’: 传递给 scipy.interpolate.interp1d。这些方法使用索引的数值。‘polynomial’ 和 ‘spline’ 都要求您还指定一个顺序（int），例如 ，df.interpolate(method='polynomial', order=5)

​			'krogh'，'piecewise_polynomial'，'spline'，'pchip'，'akima'：环绕类似名称的SciPy插值方法。请参阅注释。

​			'from_derivatives'：指 scipy.interpolate.BPoly.from_derivatives，

​	***axis***：**{{0 or ‘index’, 1 or ‘columns’, None}}, default None**

​		沿轴进行interpolate。

​	***limit***：**int, optional**

​		要填充的连续NaN的最大数量。必须大于0。

​	***inplace***：**bool, default False**

​		尽可能更新数据。

​	***limit_direction***：**{{‘forward’, ‘backward’, ‘both’}}, Optional**

​		将沿该方向填充连续的NaN。

​			如果指定了限制:

​				如果‘ method’是‘ pad’或‘ ffill’，‘ limit _ direction’必须是‘ forward’。

​				如果‘ method’是‘ backfill’或‘ bfill’，‘ limit _ direction’必须是‘ backwards’。

​			如果没有指定“限制”:

​				如果‘ method’是‘ backfill’或‘ bfill’，默认值是‘ backward’

​				否则默认值是‘ forward’

​	***limit_area*** ：**{{**None**, ‘inside’, ‘outside’}}, default None**

​		如果指定了限制，则连续的NaN将填充此限制。

​			None：无填充限制。

​			‘inside’：仅填充有效值（interpolate）包围的NaN。

​			‘outside’: 仅在有效值之外（extrapolate）填充NaN。

​	***downcast*** ：**optional, ‘infer’ or None, defaults to None**

​		如果可能，请向下转换dtype。

​	***\*kwargs**：关键字参数传递给插值函数。

注意：了解更多关于他们行为的信息，see the [SciPy documentation](https://docs.scipy.org/doc/scipy/reference/interpolate.html#univariate-interpolation) and [SciPy tutorial](https://docs.scipy.org/doc/scipy/reference/tutorial/interpolate.html).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.interpolate.html)

#### **==DataFrame.isna\isnull==**()

###### 检测缺失值。返回一个布尔值相同大小的对象，指示值是否为NA。NA值（例如,None或numpy.NaN）被映射为True值。其他所有内容都映射为False值。诸如空字符串之类的字符''或numpy.inf不被视为NA值的字符（除非您设置）。pandas.options.mode.use_inf_as_na = True

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.isna.html)

#### **==DataFrame.notna\notnull==**()

###### 检测现有（非缺失）值。返回一个布尔值相同大小的对象，指示值是否不是NA。非缺失值将映射为True。诸如空字符串之类的字符''或numpy.inf不视为NA值的字符（除非设置pandas.options.mode.use_inf_as_na = True) 。NA值(例如，None或numpy.NaN)被映射为False值。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.notna.html)

