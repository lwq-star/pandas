#### **==DataFrame.add\sub\mul\div\truediv\floordiv\mod\pow==**(other, axis='columns', level=None, fill_value=None)

###### 加法(+)\减法(-)\乘法(*)\除法(/)\除法(/)\整除(//)\取余(%)\幂(**)\dataframe和其他元素。支持用fill_value替换其中一个输入中缺失的数据。使用反向版本，r…。在灵活的包装器(add, sub, mul, div, mod, pow)到算术运算符:+，-，*，/，//，%，**。不匹配的指数将联合在一起。

##### 参数设置：

​	***other***：**scalar, sequence, Series, or DataFrame** 

​		任何单个或多个元素数据结构，或类似列表对象。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}**

​		是否通过index(0 或 ‘index’)或columns(1 or ‘columns’)进行比较。对于Series输入，axis匹配Series索引。

​	***level***：**int or label**

​		跨level广播，匹配传递的MultiIndex level的索引值。

​	***fill_value***：**float or None, default None**

​		在计算之前，用这个值填充现有的缺失值(NaN)，以及成功进行DataFrame对齐所需的任何新元素。如果两个对应的DataFrame位置中的数据都丢失，则结果将丢失。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.add.html)

#### **==DataFrame.dot==**(other)

###### 计算DataFrame与其他之间的矩阵乘法。此方法计算DataFrame与其他Series，DataFrame或numpy数组的值之间的矩阵乘积。

##### 参数设置：

​	***other***：**Series, DataFrame or array-like**

​		用于计算矩阵乘积的另一个对象。

##### 注意：

DataFrame和其他的维度必须兼容才能计算矩阵乘法。此外，DataFrame的列名称和其他索引必须包含相同的值，因为它们将在乘法之前对齐。Series的dot方法计算内积，而不是此处的矩阵乘积。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dot.html)

#### **==DataFrame.lt\gt\le\ge\ne\eq==**(other, axis='columns', level=None)

###### 获取小于(<)\大于(>)\小于等于(<=)\大于等于(>=)\不等于(!=)\等于(==)dataframe和其他元素形式的值。在灵活的包装器（eq，ne，le，lt，ge，gt）中，用于比较运算符。等效于 ==，=！，<=，<，> =，>，并支持选择轴（行或列）和级别进行比较。不匹配的索引将合并在一起。 NaN值被认为是不同的（即NaN != NaN）

##### 参数设置：

​	***other***：**scalar, sequence, Series, or DataFrame**

​		任何单个或多个元素的数据结构，或类似列表的对象。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default ‘columns’**

​		是按索引（0或'index'）还是按columns（1或'columns'）进行比较。

​	***level***：**int or label**

​		在一个级别上广播，在传递的MultiIndex级别上匹配索引值。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.lt.html)

#### **==DataFrame.ewm==**(com=None, span=None, halflife=None, alpha=None, min_periods=0, adjust=True, ignore_na=False, axis=0, times=None)

###### 提供指数加权函数。可用的EW功能：mean（），var（），std（），corr（），cov（）。必须提供质心(com)、跨度(span)、半衰期(half-life)和alpha值之一。

##### 参数设置：

​	***com***：**float, optional**

​		根据质心指定衰减， α=1/(1+com), for com≥0。

​	***span***：**float, optional**

​		根据范围指定衰减， α=2/(span+1), for span≥1。

​	***halflife***：**float, str, timedelta, optional**

​		根据半衰期指定衰减， α=1−exp(log(0.5)/halflife),forhalflife>0。如果指定了时间，则观察到其值的时间单位（str或timedelta）。仅适用于均值（）和halflife value，不适用于其他功能。

​	***alpha***：**float, optional**

​		直接指定平滑系数α， 0<α≤1。

​	***min_periods***：**int, default 0**

​		窗口中具有值的最小观察数（否则结果为NA）。

​	***adjust***：**bool, default True**

​		是否除以开始阶段的衰减调整因子，以解释相对权重的不平衡(将EWMA视为移动平均线)。

​		当adjust = True（默认）时，将使用权重(1-α)^(n-1), (1-α)^(n-2),...1-α, 1来计算加权平均值。

​		当adjust = False时，按照下式递归计算加权平均值：weightd_average[0] = arg[0];weighted_avreaged[i] = (1-α) * weighted_average[i-1] + α * arg[i]

​	***ignore_na***：**bool, default False**

​		计算权重时忽略缺失值；指定True可重现0.15.0之前的行为。

​		当ignore_na = False时，权重基于绝对值位置。

​		当ignore_na = True时，权重基于相对值位置。

​	***axis***：**{0, 1}, default 0**

​	***times***：**str, np.ndarray, Series, default None**

​		与观测值对应的时间。必须是单调递增的和日期时间64[ ns ] d 类型。如果 str，则为 DataFrame 中表示时间的列的名称。如果一维数组类似，则为与观测值形状相同的序列。只适用于mean()。

##### 注意：

More details can be found at: [Exponentially weighted windows](https://pandas.pydata.org/docs/user_guide/window.html#window-exponentially-weighted).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.ewm.html)

**DataFrame.abs()**

返回一个 Series/DataFrame，每个元素的绝对数值。此函数只适用于全部为数字的元素。对于复数输入，1.2 + 1j，绝对值是
$$
\sqrt{a^2+b^2}
$$

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.abs.html)

#### **==DataFrame.corr==**(method='pearson', min_periods=1)

###### 计算列的成对相关性，不包括NA/null值。

##### 参数设置：

​	***method***：**{‘pearson’, ‘kendall’, ‘spearman’} or callable**

​		 pearson：标准相关系数

​		 kendall：Kendall Tau相关系数

​		 spearman：Spearman等级相关

 		callable：可输入两个1d ndarray来调用并返回一个float。

​	***min_periods***：**int, optional**

​		观察每对列所需的最小数，以获得有效结果。目前仅适用于pearson和spearman correlation

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.corr.html)

#### **==DataFrame.corrwith==**(other, axis=0, drop=False, method='pearson')

###### 用于计算两个DataFrame对象的行或列之间的成对相关。如果两个DataFrame 对象的形状不同，则对应的相关值将为NaN值。

##### 参数设置：

​	***other***：**DataFrame, Series**

​		用于计算相关性的对象。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		使用.0或“index”来按列计算，1或“columns”按行计算。

​	***drop***：**bool, default False**

​		从结果删除缺失指数。

​	***method***： {'pearson'，'kendall'，'spearman'}或callable

​		 pearson：标准相关系数

​		 kendall：Kendall Tau相关系数

​		 spearman：Spearman等级相关

​		 callable：可输入两个1d ndarray来调用并返回一个float。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.corrwith.html)

#### **==DataFrame.cov==**(min_periods=None, ddof=1)

###### 计算列的成对协方差，不包括NA/null值。可以为创建的每个值的最小观察数设置阈值。与低于此阈值的观察结果的比较将返回为NaN。

##### 参数设置：

​	***min_periods***：**int, optional**

​		每对列所需的最小观察数，以获得有效结果。

​	***ddof***：**int, default 1**

​		计算中使用的除数是 n-ddof，其中 n 表示元素的数目。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.cov.html)

#### **==DataFrame.cummax\cummin\cumprod\cumsum==**(axis=None, skipna=True, *args, **kwargs)

###### 返回 DataFrame 或 Series 轴上的累积最大值。返回包含累积最大值\累积最小值\累积积\累积和的相同大小的 DataFrame 或序列。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		索引或轴的名称k。0等于None或' index '。

​	***skipna***：**bool, default True**

​		排除NA/null值。如果整个行/列是NA，那么结果将是NA。

​	***args, \**kwargs**：附加关键字没有效果，但是可以接受与NumPy兼容。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.cummax.html)

#### **==DataFrame.describe==**(percentiles=None, include=None, exclude=None, datetime_is_numeric=False)

###### 生成描述性统计数据，总结数据集分布的集中趋势，分散和形状，不包括 NaN值。

##### 参数设置：

​	***Percentiles***：**list-like of numbers, optional**

​		要包含在输出中的百分位数。全部应该介于0和1之间。默认值为 ，返回第25，第50和第75百分位数。

​	***include***：**‘all’, list-like of dtypes or None (default), optional**

​		要包含在结果中的数据类型的白名单。被忽略了Series。以下是选项：

​			'all'：输入的所有列都将包含在输出中。

​			类似于dtypes的列表：将结果限制为提供的数据类型。将结果限制为数字类型提交numpy.number。要将其限制为对象列，请提交numpy.object数据类型。字符串也可以以select_dtypes（例如df.describe(include=['O'])）的方式使用。要选择pandas分类列，请使用'category'

​			None (default) ：结果将包括所有数字列。

​	***exclude***：**list-like of dtypes or None (default), optional,**

​		要从结果中省略的黑色数据类型列表。被忽略了Series。以下是选项：

​			类似于dtypes的列表：从结果中排除提供的数据类型。要排除数字类型提交numpy.number。要排除对象列，请提交数据类型numpy.object。字符串也可以以select_dtypes（例如df.describe(include=['O'])）的方式使用。要排除pandas分类列，请使用'category'

​			None (default)：结果将不包含任何内容。

​	***datetime_is_numeric***：**bool, default False**

​		是否将日期时间 dtypes 视为数值。这将影响为该列计算的统计信息。对于 DataFrame 输入，这还控制默认情况下是否包含日期时间列。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)

#### ==**DataFrame.kurt**\kurtosis==**(axis=None, skipna=None, level=None, numeric_only=None, **kwargs)

###### 使用Fisher的峰度定义（正常的峰度== 0.0）在请求的轴上返回无偏峰度。由N-1归一化。

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​		要应用的功能的轴。

​	***skipna***：**bool, default True**

​		是否计算结果时排除NA / null值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

​	***numeric_only***：**bool, default None**

​		仅包括float，int，boolean列。如果为None，将尝试使用所有内容，然后仅使用数字数据。未针对Series实施。

​	***\*kwargs**：要传递给函数的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.kurt.html)

#### **==DataFrame.mad==**(axis=None, skipna=None, level=None)

###### 返回所请求轴上值的平均绝对偏差。

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​		要应用于的函数的轴。

​	***skipna***：**bool, default None**

​		在计算结果时是否排除 NA/null 值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.mad.html)

#### **==DataFrame.max\mean\median\min==**(axis=None, skipna=None, level=None, numeric_only=None, **kwargs)

###### 在请求的轴上返回最大值\平均值\中位数\最小值。如果你想要最大值的索引，使用 idxmax，这相当于 numpy.ndarray 方法 argmax。

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​		要应用的功能的轴。

​	***skipna***：**bool, default True**

​		是否计算结果时排除NA / null值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

​	***numeric_only***：**bool, default None**

​		仅包括float，int，boolean列。如果为None，将尝试使用所有内容，然后仅使用数字数据。未针对Series实施。

​	***\*kwargs**：要传递给函数的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.max.html)

#### **==DataFrame.mode==**(axis=0, numeric_only=False, dropna=True)

###### 获取沿选定轴的每个元素的mode(s) 。一组值的mode是最常出现的值。它可以是多个值。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		搜索mode时要迭代的axis：1) 0或'index'：获取各列的mode，2) 1或'columns'：获取每一行的mode。

​	***numeric_only***：**bool, default False**

​		如果为True，则仅适用于数字列。

​	***dropna***：**bool, default True**

​		不要考虑NaN / NaT的计数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.mode.html)

#### **==DataFrame.pct_change==**(periods=1, fill_method='pad', limit=None, freq=None, **kwargs)

###### 当前元素与前一个元素之间的百分比变化。默认情况下，计算与前一行相比的百分比变化。这在比较元素时间序列中的变化百分比时很有用。

##### 参数设置：

​	***periods***：**int, default 1**

​		形成百分比变化所需的时间。

​	***fill_method***：**str, default ‘pad’**

​		如何在计算百分比更改之前处理NAs

​	***limit***：**int, default None**

​		停止前要填充的连续NAs的数量。

​	***freq***：**DateOffset, timedelta, or str, optional**

​		时间序列API开始使用的增量（例如,"M"或BDay()）。

​	***\*kwargs**：其他关键字参数将传递到 DataFrame.shift或Series.shift中。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pct_change.html)

#### **==DataFrame.prod\product\sum==**(axis=None, skipna=None, level=None, numeric_only=None, min_count=0, **kwargs)

###### 返回所请求轴上值的乘积\总和。

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​		要应用的功能的轴。

​	***skipna***：**bool, default True**

​		是否计算结果时排除NA / null值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

​	***numeric_only***：**bool, default None**

​		仅包括float，int，boolean列。如果为None，将尝试使用所有内容，然后仅使用数字数据。未针对Series实施。

​	***min_count***：**int, default 0**

​		执行操作所需的有效值数量。如果少于 min_count非NA值，则结果将为NA。默认值0，这意味着全NA或空Series的总和为0，全NA或空Series 的乘积为1。

​	***\*kwargs**：要传递给函数的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.prod.html)

#### **==DataFrame.quantile==**(q=0.5, axis=0, numeric_only=True, interpolation='linear')

###### 在请求的轴上给定分位数的返回值。

##### 参数设置：

​	***q***：**float or array-like, default 0.5 (50% quantile)**

​		要计算的quantile值在 0 <= q <= 1之间。

​	***axis***：**{0, 1, ‘index’, ‘columns’}, default 0**

​		行为0或' index '，列为1或'columns'。

​	***numeric_only***：**bool, default True**

​		如果为False，也将计算datetime和timedelta数据的quantile。

​	***interpolation***: {‘linear’, ‘lower’, ‘higher’, ‘midpoint’, ‘nearest’}

​		这个可选参数指定了当所需quantile位于两个数据点i和j之间时要使用的插值方法:

​			\1) linear: i + (j - i) *fraction，其中分数是指数中被i和j包围的小数部分。

​			\2) lower: i

​			\3) higher: j

​			\4) nearest: i或j，以最接近的为准。

​			\5) midpoint: (i + j) / 2 

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.quantile.html)

#### **==DataFrame.sem\std\var==**(axis=None, skipna=None, level=None, ddof=1, numeric_only=None, **kwargs)

###### 返回所要求的轴上的平均值的无偏标准误差\样本标准偏差\无偏方差。默认情况下使用 n-1规范化。这可以通过使用 ddof 参数来更改。若要具有与 numpy.std 相同的行为，请使用 ddof = 0(而不是默认的 ddof = 1)

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​	***skipna***：**bool, default True**

​		是否计算结果时排除NA / null值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

​	***ddof***：**int, default 1**

​		Delta 自由度。计算中使用的除数是 n-ddof，其中 n 表示元素的数量。

​	***numeric_only***：**bool, default None**

​		对于DataFrame对象，如果设置为True，则仅对数字列进行排名。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sem.html)

#### ==**DataFrame.skew**==(axis=None, skipna=None, level=None, numeric_only=None, **kwargs)

###### 在请求的轴上返回无偏差的偏度

##### 参数设置：

​	***axis***：**{index (0), columns (1)}**

​		要应用的功能的轴。

​	***skipna***：**bool, default True**

​		是否计算结果时排除NA / null值。

​	***level***：**int or level name, default None**

​		如果轴是MultiIndex（分层），则沿特定级别计数，并折叠为Series。

​	***numeric_only***：**bool, default None**

​		仅包括float，int，boolean列。如果为None，将尝试使用所有内容，然后仅使用数字数据。未针对Series实施。

​	***\*kwargs**：要传递给函数的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.skew.html)

