- [**==DataFrame.groupby==**(by=None, axis=0, level=None, as_index=True, sort=True, group_keys=True, squeeze=NoDefault.no_default, observed=False, dropna=True)](#dataframegroupbybynone-axis0-levelnone-as_indextrue-sorttrue-group_keystrue-squeezenodefaultno_default-observedfalse-dropnatrue)
    - [使用映射器或按Series列对DataFrame或Series进行分组。分组操作涉及拆分对象，应用功能以及组合结果的某种组合。这可用于对大量数据进行分组并在这些组上进行计算操作。](#使用映射器或按series列对dataframe或series进行分组分组操作涉及拆分对象应用功能以及组合结果的某种组合这可用于对大量数据进行分组并在这些组上进行计算操作)
  - [参数设置：](#参数设置)
  - [注意：See the user guide for more.](#注意see-the-user-guide-for-more)
- [官网](#官网)
- [**==DataFrame.rolling==**(window, min_periods=None, center=False, win_type=None, on=None, axis=0, closed=None, method='single')](#dataframerollingwindow-min_periodsnone-centerfalse-win_typenone-onnone-axis0-closednone-methodsingle)
    - [提供滚动窗口计算。](#提供滚动窗口计算)
  - [参数设置：](#参数设置-1)
  - [注意：](#注意)
- [官网](#官网-1)
- [**==DataFrame.expanding==**(min_periods=1, center=None, axis=0, method='single')](#dataframeexpandingmin_periods1-centernone-axis0-methodsingle)
    - [提供expanding转换。相对于rolling，expanding只有一个窗口，它的元素个数是不断增加的。](#提供expanding转换相对于rollingexpanding只有一个窗口它的元素个数是不断增加的)
  - [参数设置：](#参数设置-2)
- [官网](#官网-2)
- [**==DataFrame.pivot==**(index=None, columns=None, values=None)](#dataframepivotindexnone-columnsnone-valuesnone)
    - [返回按给定索引/列值组织的重新构造的DataFrame。根据列值重塑数据(生成一个 "pivot" 表)。使用来自指定索引/列的惟一值来形成结果DataFrame的轴。此函数不支持数据聚合，多个值将导致列中的多索引。](#返回按给定索引列值组织的重新构造的dataframe根据列值重塑数据生成一个-pivot-表使用来自指定索引列的惟一值来形成结果dataframe的轴此函数不支持数据聚合多个值将导致列中的多索引)
  - [参数设置：](#参数设置-3)
- [官网](#官网-3)
- [**==DataFrame.pivot_table==**(values=None, index=None, columns=None, aggfunc='mean', fill_value=None, margins=False, dropna=True, margins_name='All', observed=False, sort=True)](#dataframepivot_tablevaluesnone-indexnone-columnsnone-aggfuncmean-fill_valuenone-marginsfalse-dropnatrue-margins_nameall-observedfalse-sorttrue)
    - [创建电子表格样式的pivot table作为DataFrame。pivot table中的级别将存储在结果DataFrame的索引和列上的MultiIndex对象（分层索引）中。](#创建电子表格样式的pivot-table作为dataframepivot-table中的级别将存储在结果dataframe的索引和列上的multiindex对象分层索引中)
  - [参数设置：](#参数设置-4)
- [官网](#官网-4)
- [**==DataFrame.stack==**(level=- 1, dropna=True)](#dataframestacklevel--1-dropnatrue)
    - [从列到索引堆叠指定级别。返回一个经过重整的DataFrame或Series，与当前DataFrame相比，该DataFrame或Series具有一个或多个新的最内层的多层索引。通过旋转当前DataFrame的列来创建新的最内层：](#从列到索引堆叠指定级别返回一个经过重整的dataframe或series与当前dataframe相比该dataframe或series具有一个或多个新的最内层的多层索引通过旋转当前dataframe的列来创建新的最内层)
  - [参数设置：](#参数设置-5)
- [官网](#官网-5)
- [**==DataFrame.unstack==**(level=- 1, fill_value=None)](#dataframeunstacklevel--1-fill_valuenone)
    - [Pivot(必要的分层)索引标签的一个级别。返回具有列标签新级别的DataFrame，其最内部级别由pivoted索引标签组成。如果索引不是多索引，则输出将是一个Series(当列不是多索引时，类似于stack)。](#pivot必要的分层索引标签的一个级别返回具有列标签新级别的dataframe其最内部级别由pivoted索引标签组成如果索引不是多索引则输出将是一个series当列不是多索引时类似于stack)
  - [参数设置：](#参数设置-6)
- [官网](#官网-6)
- [**==DataFrame.melt==**(id_vars=None, value_vars=None, var_name=None, value_name='value', col_level=None, ignore_index=True)](#dataframemeltid_varsnone-value_varsnone-var_namenone-value_namevalue-col_levelnone-ignore_indextrue)
    - [这个函数对于将DataFrame转换成这样一种格式非常有用，其中一个或多个列是标识符变量(id_vars)，而所有其他列(被认为是测量变量(value_vars))都"unpivoted"到行轴，只留下两个非标识符列"variable"和"value"。](#这个函数对于将dataframe转换成这样一种格式非常有用其中一个或多个列是标识符变量id_vars而所有其他列被认为是测量变量value_vars都unpivoted到行轴只留下两个非标识符列variable和value)
  - [参数设置：](#参数设置-7)
- [官网](#官网-7)
- [**==DataFrame.explode==**(column, ignore_index=False)](#dataframeexplodecolumn-ignore_indexfalse)
    - [将类似列表的每个元素转换为一行，从而复制索引值。](#将类似列表的每个元素转换为一行从而复制索引值)
  - [参数设置：](#参数设置-8)
- [官网](#官网-8)
- [**==DataFrame.squeeze==**(axis=None)](#dataframesqueezeaxisnone)
    - [将1维轴对象Squeeze成标量(scalars)。具有单个元素的Series或数据类型被压缩为标量(scalars)。具有单列或单行的数据被Squeeze为一个Series。否则对象不变。当不知道对象是Series还是DataFrame，但知道它只有一个列时，此方法最有用。在这种情况下，您可以安全地调用squeeze，以确保您拥有一个Series。](#将1维轴对象squeeze成标量scalars具有单个元素的series或数据类型被压缩为标量scalars具有单列或单行的数据被squeeze为一个series否则对象不变当不知道对象是series还是dataframe但知道它只有一个列时此方法最有用在这种情况下您可以安全地调用squeeze以确保您拥有一个series)
  - [参数设置：](#参数设置-9)
- [官网](#官网-9)
- [**==DataFrame.to_xarray==**()](#dataframeto_xarray)
    - [从 pandas 对象返回一个 xarray 对象。](#从-pandas-对象返回一个-xarray-对象)
- [官网](#官网-10)
- [**==DataFrame.transpose\T==**(*args, copy=False)](#dataframetransposetargs-copyfalse)
    - [转置索引和列。通过将行写为列将DataFrame反映在其主要对角线上，反之亦然。该属性T是方法的访问器](#转置索引和列通过将行写为列将dataframe反映在其主要对角线上反之亦然该属性t是方法的访问器)
  - [参数设置：](#参数设置-10)
- [官网](#官网-11)
- [**==DataFrame.assign==**(**kwargs)](#dataframeassignkwargs)
    - [为DataFrame分配新列。返回一个新对象，该对象包含除新列之外的所有原始列。重新分配的现有列将被覆盖。](#为dataframe分配新列返回一个新对象该对象包含除新列之外的所有原始列重新分配的现有列将被覆盖)
  - [参数设置：](#参数设置-11)
- [官网](#官网-12)
- [**==DataFrame.compare==**(other, align_axis=1, keep_shape=False, keep_equal=False)](#dataframecompareother-align_axis1-keep_shapefalse-keep_equalfalse)
    - [与另一个DataFrame进行比较并显示差异。](#与另一个dataframe进行比较并显示差异)
  - [参数设置：](#参数设置-12)
- [官网](#官网-13)

#### **==DataFrame.groupby==**(by=None, axis=0, level=None, as_index=True, sort=True, group_keys=True, squeeze=NoDefault.no_default, observed=False, dropna=True)

###### 使用映射器或按Series列对DataFrame或Series进行分组。分组操作涉及拆分对象，应用功能以及组合结果的某种组合。这可用于对大量数据进行分组并在这些组上进行计算操作。

##### 参数设置：

​	***by***： **mapping, function, label, or list of labels**

​		用于确定分组依据的分组。如果by是函数，则在对象索引的每个值上调用它。如果by是dict或Series，则将使用Series或dict VALUES来确定组（将Series的值首先对齐；请参见.align()方法）。如果传递了ndarray，则按原样使用这些值来确定组。标签或标签列表可以按中的列传递给分组self。注意，元组被解释为（单个）key。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		沿rows (0)或columns (1)拆分。

​	***level***：**int, level name, or sequence of such, default None**

​		如果axis是MultiIndex（分层），则按一个或多个特定级别分组。

​	***as_index***：**bool, default True**

​		对于聚合输出，是否返回带有组标签的对象作为索引。仅与DataFrame输入有关。as_index = False实际上是“ SQL风格”的分组输出。

​	***sort***：**bool, default True**

​		是否排序组键。关闭此功能可获得更好的性能。请注意，这不会影响每个组中观察的顺序。Groupby保留每个组中行的顺序。

​	***group_keys***：**bool, default True**

​		调用apply时，是否将组键添加到索引以识别片段。

​	***observed***：**bool, default False**

​		仅当任何groupers为Categoricals时才适用。如果为True：仅显示分类groupers的观测值。如果为False：显示分类groupers的所有值。

​	***dropna***：**bool, default True**

​		如果为 True，并且组键包含 NA 值，则将删除 NA 值和行/列。如果为 False，则 NA 值也将被视为组中的键

##### 注意：See the [user guide](https://pandas.pydata.org/pandas-docs/stable/groupby.html) for more.

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html)

#### **==DataFrame.rolling==**(window, min_periods=None, center=False, win_type=None, on=None, axis=0, closed=None, method='single')

###### 提供滚动窗口计算。

##### 参数设置：

​	***window***：**int, offset, or BaseIndexer subclass**

​		移动窗口的大小。这是用于计算统计量的观测数。每个窗口的大小都是固定的。如果它是一个offset，那么这将是每个窗口的时间段。每个窗口的大小将根据时间段内的观察结果而变化。这只对类似日期时间的索引有效。如果传递了BaseIndexer子类，则根据定义的get_window_bounds方法计算窗口边界。其他rolling关键字参数，即min_period、center和closed将被传递给get_window_bounds。

​	***min_periods***：**int, default None**

​		窗口中需要有一个值的最小观察次数(否则结果为NA)。对于由偏移量指定的窗口，min_period默认为1。否则，min_period将默认为窗口的大小。

​	***center***: **bool, default False**

​		是否把窗口的标签设置为居中。

​	***win_type***: **str, default None**

​		提供一个窗口类型。如果没有，所有的点都是均匀加权的。有关详细信息，请参阅下面的注释。

​	***on***: **str, optional**

​		对于 DataFrame，这是一个类似于 datetime 的列或 Index 级别，用于计算滚动窗口，而不是 DataFrame 的索引。因为整数索引不用于计算滚动窗口，因此整数列被忽略并从结果中排除。

​	***axis***: **int or str, default 0**

​		即对列进行计算

​	***closed***：**str, default None**

​		使区间在‘right’, ‘left’, ‘both’ 或者 ‘neither’为闭。默认为右。

​	***method***：**str {‘single’, ‘table’}, default ‘single’**

​		对单个列或行('single')或整个对象('table')执行滚动操作。只有在方法调用中指定 engine = ‘ numba’时，才会实现这个参数。

##### 注意：

要了解更多关于偏移量和频率字符串，请看这个 [this link](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#offset-aliases).如果 win _ type = None，所有的点都是均匀加权的; 否则，win _ type 可以接受任意 [scipy.signal window function](https://docs.scipy.org/doc/scipy/reference/signal.windows.html#module-scipy.signal.windows).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rolling.html)

#### **==DataFrame.expanding==**(min_periods=1, center=None, axis=0, method='single')

###### 提供expanding转换。相对于rolling，expanding只有一个窗口，它的元素个数是不断增加的。

##### 参数设置：

​	***min_periods***：**int, default 1**

​		窗口中具有值的最小观察数（否则结果为NA）。

​	***center***：**bool, default False**

​		是否将标签设置在窗口的中央。

​	***axis***：**int or str, default 0**

​	***method***：**str {‘single’, ‘table’}, default ‘single’**

​		对单个列或行('single')或整个对象('table')执行滚动操作。只有在方法调用中指定 engine = ‘ numba’时，才会实现这个参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.expanding.html)

#### **==DataFrame.pivot==**(index=None, columns=None, values=None)

###### 返回按给定索引/列值组织的重新构造的DataFrame。根据列值重塑数据(生成一个 "pivot" 表)。使用来自指定索引/列的惟一值来形成结果DataFrame的轴。此函数不支持数据聚合，多个值将导致列中的多索引。

##### 参数设置：

​	***index***：**str or object or a list of str, optional**

​		用于制作新frame索引的行。如果为None，则使用现有索引。

​	***columns***：**str or object or a list of str**

​		用于制作新frame索引的列

​	***values***：**str, object or a list of the previous, optional**

​		用于填充新frame值的列。如果未指定，将使用所有剩余的列，并且结果将具有按层次结构索引的列。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pivot.html)

#### **==DataFrame.pivot_table==**(values=None, index=None, columns=None, aggfunc='mean', fill_value=None, margins=False, dropna=True, margins_name='All', observed=False, sort=True)

###### 创建电子表格样式的pivot table作为DataFrame。pivot table中的级别将存储在结果DataFrame的索引和列上的MultiIndex对象（分层索引）中。

##### 参数设置：

​	***values*** ：**column to aggregate, optional**

​	***index***：**column, Grouper, array, or list of the previous**

​		如果传递数组，则其长度必须与数据长度相同。该列表可以包含任何其他类型（列表除外）。在pivot table索引上进行分组的键。如果传递了数组，则其使用方式与列值相同。

​	***columns***：**column, Grouper, array, or list of the previous**

​		如果传递数组，则其长度必须与数据长度相同。该列表可以包含任何其他类型（列表除外）。在pivot table列上进行分组的键。如果传递了数组，则其使用方式与列值相同。

​	***aggfunc***：**function, list of functions, dict, default numpy.mean**

​		如果传递了函数列表，则生成的pivot table将具有层次结构列，其顶层是函数名称（从函数对象本身推论得出）。如果传递了dict，则键为要汇总的列，值是函数或函数列表。

​	***fill_value***：**scalar, default None**

​		用于替换缺失值的值。

​	***margins*** ：**bool, default False**

​		添加所有行/列（例如，小计/总计）。

​	***dropna*** ：**bool, default True**

​		不要包括所有条目均为NaN的列。

​	***margins_name*** ：**str, default ‘All’**

​		当margins为True时将包含总计的行/列的名称。

​	***observed***：**bool, default False**

​		仅当任何 groupers是分类者时才适用。如果为True：仅显示分类 groupers 的观测值。如果为False：显示分类 groupers 的所有值。

​	***sort***：**bool, default True**

​		指定结果是否应该排序。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pivot_table.html)

#### **==DataFrame.stack==**(level=- 1, dropna=True)

###### 从列到索引堆叠指定级别。返回一个经过重整的DataFrame或Series，与当前DataFrame相比，该DataFrame或Series具有一个或多个新的最内层的多层索引。通过旋转当前DataFrame的列来创建新的最内层：

​	\1) 如果列具有单个级别，则输出为Series；

​	\2) 如果列具有多个级别，则新索引级别取自指定级别，并且输出为DataFrame。

##### 参数设置：

​	***level***：**int, str, list, default -1**

​		从列轴堆叠到索引轴，定义为一个索引或标签，或一列索引或标签。

​	***dropna***：**bool, default True**

​		是否删除结果Frame/Series中缺少值的行。将列级堆叠到索引轴上,可以创建原始dataframe中缺少的索引和列值的组合。看到部分例子。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.stack.html)

#### **==DataFrame.unstack==**(level=- 1, fill_value=None)

###### Pivot(必要的分层)索引标签的一个级别。返回具有列标签新级别的DataFrame，其最内部级别由pivoted索引标签组成。如果索引不是多索引，则输出将是一个Series(当列不是多索引时，类似于stack)。

##### 参数设置：

​	***level***：**int, str, list, default -1**

​		要unstack的索引级别，可以通过级别名称。

​	***fill_value***：**int, str or dict**

​		如果unstack产生缺少的值，请用该值替换NaN。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.unstack.html)

#### **==DataFrame.melt==**(id_vars=None, value_vars=None, var_name=None, value_name='value', col_level=None, ignore_index=True)

###### 这个函数对于将DataFrame转换成这样一种格式非常有用，其中一个或多个列是标识符变量(id_vars)，而所有其他列(被认为是测量变量(value_vars))都"unpivoted"到行轴，只留下两个非标识符列"variable"和"value"。

##### 参数设置：

​	***id_vars***：**tuple, list, or ndarray, optional**

​		用作标识符变量的列。

​	***value_vars***：**tuple, list, or ndarray, optional**

​		要unpivot的列。如果未指定，则使用未设置为id_vars的所有列。

​	***var_name***：用于‘variable’列的名称。如果为None，则使用 frame.columns.name或‘variable’。

​	***value_name***：**scalar**

​		用于‘value’列的名称。

​	***col_level***：**int or str, optional**

​		如果列是MultiIndex，则使用此级别进行融合。

​	***ignore_index***：**bool, default True**

​		如果为true，则忽略原始索引。如果为false，则保留原始索引。索引标签将根据需要重复。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.melt.html)

#### **==DataFrame.explode==**(column, ignore_index=False)

###### 将类似列表的每个元素转换为一行，从而复制索引值。

##### 参数设置：

​	***column***：**IndexLabel**

​		列爆炸。对于多个列，指定一个非空列表，其中每个元素为 str 或 tuple，并且框架中同一行上的所有指定列及其类似列表的数据必须具有匹配的长度。

​	***ignore_index***：**bool, default False**

​		如果为true，则结果索引将标记为0,1，...，n - 1。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.explode.html)

#### **==DataFrame.squeeze==**(axis=None)

###### 将1维轴对象Squeeze成标量(scalars)。具有单个元素的Series或数据类型被压缩为标量(scalars)。具有单列或单行的数据被Squeeze为一个Series。否则对象不变。当不知道对象是Series还是DataFrame，但知道它只有一个列时，此方法最有用。在这种情况下，您可以安全地调用squeeze，以确保您拥有一个Series。

##### 参数设置：

​	**axis**：**{0 or ‘index’, 1 or ‘columns’, None}, default None**

​		一个特定squeeze的轴。默认情况下，所有长度为1的轴都被squeeze。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.squeeze.html)

#### **==DataFrame.to_xarray==**()

###### 从 pandas 对象返回一个 xarray 对象。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_xarray.html)

#### **==DataFrame.transpose\T==**(*args, copy=False)

###### 转置索引和列。通过将行写为列将DataFrame反映在其主要对角线上，反之亦然。该属性T是方法的访问器

##### 参数设置：

​	***args**：**tuple, optional**

​		接受与NumPy的兼容性。

​	**copy**：**bool, default False**

​		是否在转置后复制数据，即使对于具有单个dtype的DataFrame也是如此。转换带有混合dtypes的DataFrame将导致对象 dtype具有同构的DataFrame 。在这种情况下，始终会复制数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.transpose.html)

#### **==DataFrame.assign==**(**kwargs)

###### 为DataFrame分配新列。返回一个新对象，该对象包含除新列之外的所有原始列。重新分配的现有列将被覆盖。

##### 参数设置：

​	***\*kwargs**：**dict of {str: callable or Series}**

​		列名是关键字。如果这些值是可调用的，那么它们将在DataFrame上计算并分配给新列。可调用项不能更改输入DataFrame(不过pandas不会检查它)。如果这些值是不可调用的(例如，Series、scalar或array)，则只分配它们。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.assign.html)

#### **==DataFrame.compare==**(other, align_axis=1, keep_shape=False, keep_equal=False)

###### 与另一个DataFrame进行比较并显示差异。

##### 参数设置：

​	***other***: **DataFrame**

​		要比较的数据。

​	***align_axis***：**{0 or ‘index’, 1 or ‘columns’}, default 1**

​		确定要在哪个轴上对齐比较。

​			0, or ‘index’：有自我和他人交替划出的行。

​			1, or ‘columns’：用自己和他人交替绘制的柱子。

​	***keep_shape***：**bool, default False**

​		如果为 true，则保留所有行和列，否则只保留具有不同值的行和列。

​	***keep_equal***：**bool, default False**

​		如果为true，则结果保持相等的值。否则，等值显示为NAN。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.compare.html)
