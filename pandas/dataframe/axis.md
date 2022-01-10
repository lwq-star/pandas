- [==**DataFrame.index**==](#dataframeindex)
    - [DataFrame 的索引（行标签）](#dataframe-的索引行标签)
- [==**DataFrame.columns**==](#dataframecolumns)
    - [DataFrame的列标签](#dataframe的列标签)
- [==**DataFrame.axes**==](#dataframeaxes)
    - [返回一个表示 DataFrame 轴的列表。它将行轴标签和列轴标签作为唯一的成员。他们按此顺序返回。](#返回一个表示-dataframe-轴的列表它将行轴标签和列轴标签作为唯一的成员他们按此顺序返回)
- [官网](#官网)
- [**==DataFrame.add_prefix==**(prefix)](#dataframeadd_prefixprefix)
    - [带有字符串前缀的前缀标签。对于Series，行标签是前缀的。对于DataFrame，列标签是前缀的。](#带有字符串前缀的前缀标签对于series行标签是前缀的对于dataframe列标签是前缀的)
  - [参数设置：](#参数设置)
- [官网](#官网-1)
- [**==DataFrame.add_suffix==**(suffix)](#dataframeadd_suffixsuffix)
    - [带有字符串后缀的后缀标签。对于Series，行标签加后缀。对于DataFrame，列标签加后缀。](#带有字符串后缀的后缀标签对于series行标签加后缀对于dataframe列标签加后缀)
  - [参数设置：](#参数设置-1)
- [官网](#官网-2)
- [**==DataFrame.idxmax\idxmin==**(axis=0, skipna=True)](#dataframeidxmaxidxminaxis0-skipnatrue)
    - [返回在请求轴上第一次出现最大值\最小值的索引。不包括NA/null。](#返回在请求轴上第一次出现最大值最小值的索引不包括nanull)
  - [参数设置：](#参数设置-2)
- [官网](#官网-3)
- [==**DataFrame.reindex**==(labels=None, index=None, columns=None, axis=None, method=None, copy=True, level=None, fill_value=nan, limit=None, tolerance=None)](#dataframereindexlabelsnone-indexnone-columnsnone-axisnone-methodnone-copytrue-levelnone-fill_valuenan-limitnone-tolerancenone)
    - [使用可选的填充逻辑使DataFrame符合新索引。将NA/NaN放在上一个索引中没有值的位置。除非新索引等于当前索引和，否则将生成一个新对象 copy=False](#使用可选的填充逻辑使dataframe符合新索引将nanan放在上一个索引中没有值的位置除非新索引等于当前索引和否则将生成一个新对象-copyfalse)
  - [参数设置：](#参数设置-3)
- [官网](#官网-4)
- [==**DataFrame.reindex_like**==(other, method=None, copy=True, limit=None, tolerance=None)](#dataframereindex_likeother-methodnone-copytrue-limitnone-tolerancenone)
    - [返回具有匹配索引的对象作为其他对象。使对象在所有轴上都具有相同的索引。可选的填充逻辑，将NaN放在上一个索引中没有值的位置。除非新索引等于当前索引并且copy=False，否则将生成一个新对象。与调用. reindex (index = other.index，columns = other.columns，...)相同。](#返回具有匹配索引的对象作为其他对象使对象在所有轴上都具有相同的索引可选的填充逻辑将nan放在上一个索引中没有值的位置除非新索引等于当前索引并且copyfalse否则将生成一个新对象与调用-reindex-index--otherindexcolumns--othercolumns相同)
  - [参数设置：](#参数设置-4)
- [官网](#官网-5)
- [==**DataFrame.rename**==(mapper=None, index=None, columns=None, axis=None, copy=True, inplace=False, level=None, errors='ignore')](#dataframerenamemappernone-indexnone-columnsnone-axisnone-copytrue-inplacefalse-levelnone-errorsignore)
    - [更改轴标签。Function/dict值必须唯一（1对1）。dict/Series中未包含的标签将保持原样。列出的其他标签不会引发错误。](#更改轴标签functiondict值必须唯一1对1dictseries中未包含的标签将保持原样列出的其他标签不会引发错误)
  - [参数设置：](#参数设置-5)
- [官网](#官网-6)
- [**==DataFrame.rename_axis==**(mapper=None, index=None, columns=None, axis=None, copy=True, inplace=False)](#dataframerename_axismappernone-indexnone-columnsnone-axisnone-copytrue-inplacefalse)
    - [设置索引或列的轴的名称。](#设置索引或列的轴的名称)
  - [参数设置：](#参数设置-6)
- [官网](#官网-7)
- [==**DataFrame.reset_index**==(level=None, drop=False, inplace=False, col_level=0, col_fill='')](#dataframereset_indexlevelnone-dropfalse-inplacefalse-col_level0-col_fill)
    - [重置索引或索引的一个级别。重置DataFrame的索引，并使用默认索引。如果DataFrame有一个MultiIndex，此方法可以删除一个或多个级别。](#重置索引或索引的一个级别重置dataframe的索引并使用默认索引如果dataframe有一个multiindex此方法可以删除一个或多个级别)
  - [参数设置：](#参数设置-7)
- [官网](#官网-8)
- [**==DataFrame.set_axis==(**labels, axis=0, inplace=False)](#dataframeset_axislabels-axis0-inplacefalse)
    - [将所需的索引分配给给定的轴。可以通过分配类似列表或索引的方式来更改列标签或行标签的索引。](#将所需的索引分配给给定的轴可以通过分配类似列表或索引的方式来更改列标签或行标签的索引)
  - [参数设置：](#参数设置-8)
- [官网](#官网-9)
- [**==DataFrame.set_index==**(keys, drop=True, append=False, inplace=False, verify_integrity=False)](#dataframeset_indexkeys-droptrue-appendfalse-inplacefalse-verify_integrityfalse)
    - [使用现有列设置DataFrame索引。使用一个或多个现有的列或数组(正确的长度)设置DataFrame索引(行标签)。索引可以替换现有索引或在其上展开](#使用现有列设置dataframe索引使用一个或多个现有的列或数组正确的长度设置dataframe索引行标签索引可以替换现有索引或在其上展开)
  - [参数设置：](#参数设置-9)
- [官网](#官网-10)
- [**==DataFrame.droplevel==**(level, axis=0)](#dataframedroplevellevel-axis0)
    - [返回删除指定的索引/列级别的DataFrame。](#返回删除指定的索引列级别的dataframe)
  - [参数设置：](#参数设置-10)
- [官网](#官网-11)
- [**==DataFrame.reorder_levels==**(order, axis=0)](#dataframereorder_levelsorder-axis0)
    - [使用输入顺序重新排列索引levels。可能不会删除或重复levels。](#使用输入顺序重新排列索引levels可能不会删除或重复levels)
  - [参数设置：](#参数设置-11)
- [官网](#官网-12)
- [**==DataFrame.sort_index==**(axis=0, level=None, ascending=True, inplace=False, kind='quicksort', na_position='last', sort_remaining=True, ignore_index=False, key=None)](#dataframesort_indexaxis0-levelnone-ascendingtrue-inplacefalse-kindquicksort-na_positionlast-sort_remainingtrue-ignore_indexfalse-keynone)
    - [按标签(沿轴)对对象进行排序。如果 inplace 参数为 False，则返回按标签排序的新 DataFrame，否则将更新原始 DataFrame 并返回 None。](#按标签沿轴对对象进行排序如果-inplace-参数为-false则返回按标签排序的新-dataframe否则将更新原始-dataframe-并返回-none)
  - [参数设置：](#参数设置-12)
- [官网](#官网-13)
- [**==DataFrame.swaplevel==**(i=- 2, j=- 1, axis=0)](#dataframeswapleveli--2-j--1-axis0)
    - [MultiIndex 中的交换级别 i 和 j。默认情况是交换索引最里面的两个级别。](#multiindex-中的交换级别-i-和-j默认情况是交换索引最里面的两个级别)
  - [参数设置：](#参数设置-13)
- [官网](#官网-14)
#### ==**DataFrame.index**==

###### DataFrame 的索引（行标签）

#### ==**DataFrame.columns**==

###### DataFrame的列标签

#### ==**DataFrame.axes**==

###### 返回一个表示 DataFrame 轴的列表。它将行轴标签和列轴标签作为唯一的成员。他们按此顺序返回。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.axes.html)

#### **==DataFrame.add_prefix==**(prefix)

###### 带有字符串前缀的前缀标签。对于Series，行标签是前缀的。对于DataFrame，列标签是前缀的。

##### 参数设置：

​	**prefix**：**str**

​		要在每个标签前添加的字符串。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.add_prefix.html)

#### **==DataFrame.add_suffix==**(suffix)

###### 带有字符串后缀的后缀标签。对于Series，行标签加后缀。对于DataFrame，列标签加后缀。

##### 参数设置：

​	**suffix**：**str**

​		每个标签后面要添加的字符串。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.add_suffix.html)

#### **==DataFrame.idxmax\idxmin==**(axis=0, skipna=True)

###### 返回在请求轴上第一次出现最大值\最小值的索引。不包括NA/null。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		行为0或'index'，列为1或'columns'

​	***skipna***：**bool, default True**

​		排除NA/null。如果整个行/列均为NA，则结果为NA。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.idxmax.html)

#### ==**DataFrame.reindex**==(labels=None, index=None, columns=None, axis=None, method=None, copy=True, level=None, fill_value=nan, limit=None, tolerance=None)

###### 使用可选的填充逻辑使DataFrame符合新索引。将NA/NaN放在上一个索引中没有值的位置。除非新索引等于当前索引和，否则将生成一个新对象 copy=False

##### 参数设置：

​	***keywords for axes***：**array-like, optional**

​		应使用关键字指定新的标签/索引，最好是索引对象，以避免重复数据。

​	***method***: **{None, ‘backfill’/’bfill’, ‘pad’/’ffill’, ‘nearest’}**

​		用于在重新索引的DataFrame中填充孔的方法。请注意：这仅适用于具有单调递增/递减索引的DataFrames/Series。

​			\1) None (default): 不填补空白

​			\2) pad / ffill: 将上一个有效观察值向前传播到下一个有效值。

​			\3) backfill / bfill: 使用下一个有效观察值填充空白。

​			\4) nearest: 使用最近的有效观测值来填补空白。

​	***copy*** : **bool, default True**

​		即使传递的索引相同，也返回一个新对象。

​	***level***：**int or name**

​		在一个级别上广播，在传递的MultiIndex级别上匹配索引值。

​	***fill_value*** : **scalar, default np.NaN**

​		用于缺失值的值。默认为NaN，但可以是任何“compatible”值。

​	***limit*** :**int, default None**

​		向前或向后填充的连续元素的最大数量。

​	***tolerance***：**optional**

​		不精确匹配的原始标签和新标签之间的最大距离。在匹配位置的索引值最符合公式abs(index[indexer] - target) <= tolerance。公差可以是一个标量值，它对所有值应用相同的tolerance;也可以是类似列表的值，它对每个元素应用可变的tolerance。list-like包括list、tuple、array、Series，并且必须与索引相同大小，其dtype必须与索引的类型完全匹配。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reindex.html)

#### ==**DataFrame.reindex_like**==(other, method=None, copy=True, limit=None, tolerance=None)

###### 返回具有匹配索引的对象作为其他对象。使对象在所有轴上都具有相同的索引。可选的填充逻辑，将NaN放在上一个索引中没有值的位置。除非新索引等于当前索引并且copy=False，否则将生成一个新对象。与调用. reindex (index = other.index，columns = other.columns，...)相同。

##### 参数设置：

​	**other**：**Object of the same data type**

​		它的行和列索引用于定义此对象的新索引。

​	**method**: **{None, ‘backfill’/’bfill’, ‘pad’/’ffill’, ‘nearest’}**

​		用于在重新索引的DataFrame中填充孔的方法。请注意：这仅适用于具有单调递增/递减索引的DataFrames/Series。

​			\1) None (default): 不填补空白

​			\2) pad / ffill: 将上一个有效观察值向前传播到下一个有效值。

​			\3) backfill / bfill: 使用下一个有效观察值填充空白。

​			\4) nearest: 使用最近的有效观测值来填补空白。

​	**copy** : **bool, default True**

​		即使传递的索引相同，也返回一个新对象。

​	**limit** :**int, default None**

​		向前或向后填充的连续元素的最大数量。

​	**tolerance**：**optional**

​		不精确匹配的原始标签和新标签之间的最大距离。在匹配位置的索引值最符合公式abs(index[indexer] - target) <= tolerance。公差可以是一个标量值，它对所有值应用相同的tolerance;也可以是类似列表的值，它对每个元素应用可变的tolerance。list-like包括list、tuple、array、Series，并且必须与索引相同大小，其dtype必须与索引的类型完全匹配。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reindex_like.html)

#### ==**DataFrame.rename**==(mapper=None, index=None, columns=None, axis=None, copy=True, inplace=False, level=None, errors='ignore')

###### 更改轴标签。Function/dict值必须唯一（1对1）。dict/Series中未包含的标签将保持原样。列出的其他标签不会引发错误。

##### 参数设置：

​	***mapper***: **dict-like or function**

​		类似于 dict 的转换或应用于该轴值的函数转换。使用映射器和轴来指定使用映射器的目标轴，或者使用索引和列。

​	***index***: **dict-like or function**

​		替代指定轴(mapper，axis = 0等价于 index = mapper)。

​	***columns***:**dict-like or function**

​		指定axis (mapper, axis=1等同于columns=mapper)的替代方法。

​	***axis***:**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		轴到目标与mapper。可以是轴名(' index '， ' columns ')或数字(0,1)，默认为' index '。

​	***copy***:**bool, default True**

​		还要复制底层数据。

​	***inplace***:**bool, default False**

​		是否返回一个新的DataFrame。如果为真，则忽略copy的值。

​	***level***:**int or level name, default None**

​		对于多索引，只能在指定的级别重命名标签。

​	***errors***:**{‘ignore’, ‘raise’}, default ‘ignore’**

​		如果‘raise’，则在类似于dict的映射器、索引或列包含正在转换的索引中不存在的标签时引发键错误。如果 ‘ignore’现有的键将被重命名，额外的键将被忽略。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rename.html)

#### **==DataFrame.rename_axis==**(mapper=None, index=None, columns=None, axis=None, copy=True, inplace=False)

###### 设置索引或列的轴的名称。

##### 参数设置：

​	**mapper** : **scalar, list-like, optional**

​		设置axis名称属性的值。

​	**index, columns** : **scalar, list-like, dict-like or function, optional**

​		标量，类似于列表，类似于dict或函数的转换，以应用于该axis的值。使用mapper和axis，可以使用mapper或index 和/或columns指定要指定的轴。

​	**axis**：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		重命名的轴。

​	**copy**：**bool, default True**

​		还要复制底层数据。

​	**inplace**：**bool, default False**

​		直接修改对象，而不是创建新的Series或DataFrame。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rename_axis.html)

#### ==**DataFrame.reset_index**==(level=None, drop=False, inplace=False, col_level=0, col_fill='')

###### 重置索引或索引的一个级别。重置DataFrame的索引，并使用默认索引。如果DataFrame有一个MultiIndex，此方法可以删除一个或多个级别。

##### 参数设置：

​	**level**：**int, str, tuple, or list, default None**

​		只从索引中删除给定的级别。默认移除所有级别。

​	**drop**：**bool, default False**

​		不要尝试向dataframe列插入索引。这会将索引重置为默认整数索引。

​	**inplace**：**bool, default False**

​		适当地修改DataFrame(不要创建新对象)。

​	**col_level**：**int or str, default 0**

​		如果列有多个级别，请确定将标签插入到哪个级别。默认情况下，它被插入到第一级。

​	**col_fill**：**object, default ‘’**

​		如果列有多个级别，请确定其他级别的命名方式。如果没有，则重复索引名。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reset_index.html)

#### **==DataFrame.set_axis==(**labels, axis=0, inplace=False)

###### 将所需的索引分配给给定的轴。可以通过分配类似列表或索引的方式来更改列标签或行标签的索引。

##### 参数设置：

​	**labels**：**list-like, Index**

​		新索引的值。

​	**axis**：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要更新的轴。值0表示行，1表示列。

​	**inplace**：**bool, default False**

​		允许或不允许对同一行进行多次抽样。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.set_axis.html)

#### **==DataFrame.set_index==**(keys, drop=True, append=False, inplace=False, verify_integrity=False)

###### 使用现有列设置DataFrame索引。使用一个或多个现有的列或数组(正确的长度)设置DataFrame索引(行标签)。索引可以替换现有索引或在其上展开

##### 参数设置：

​	**keys**：**label or array-like or list of labels/arrays**

​		此参数可以是单个列键，长度与调用DataFrame相同的单个数组，也可以是包含列键和数组的任意组合的列表。在这里，“array” 包括 [Serise](https://pandas.pydata.org/docs/reference/api/pandas.Series.html#pandas.Series)，[`Index`](https://pandas.pydata.org/docs/reference/api/pandas.Index.html#pandas.Index), `np.ndarray`, 和 [`Iterator`](https://docs.python.org/3/library/collections.abc.html#collections.abc.Iterator).

​	**drop**：**bool, default True**

​		删除要用作新索引的列。

​	**append**：**bool, default False**

​		是否将列追加到现有索引。

​	**inplace**：**bool, default False**

​		适当地修改DataFrame(不创建新对象)。

​	**verify_integrity**：**bool, default False**

​		检查新索引是否重复。否则，将检查推迟到必要时进行。设置为False将改善此方法的性能。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.set_index.html)

#### **==DataFrame.droplevel==**(level, axis=0)

###### 返回删除指定的索引/列级别的DataFrame。

##### 参数设置：

​	***level***:**int, str, or list-like**

​		如果给出了字符串，则必须是级别的名称。如果类似列表，则元素必须是级别的名称或位置索引。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		移除级别的轴。0或‘ index’: 删除列中的级别。1或“ columns”: 删除行中的级别。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.droplevel.html)

#### **==DataFrame.reorder_levels==**(order, axis=0)

###### 使用输入顺序重新排列索引levels。可能不会删除或重复levels。

##### 参数设置：

​	**order**：**list of int or list of str**

​		代表新级别order的列表。参考级别按number（position）或key（label）。

​	**axis**：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		在哪重新排序levels

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reorder_levels.html)

#### **==DataFrame.sort_index==**(axis=0, level=None, ascending=True, inplace=False, kind='quicksort', na_position='last', sort_remaining=True, ignore_index=False, key=None)

###### 按标签(沿轴)对对象进行排序。如果 inplace 参数为 False，则返回按标签排序的新 DataFrame，否则将更新原始 DataFrame 并返回 None。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要排序的轴。值0标识行，1标识列。

​	***level***：**int or level name or list of ints or list of level names**

​		如果不为None，则按指定索引级别的值排序。

​	***ascending***：**bool or list-like of bools, default True**

​		升序和降序排序。指定多个排序顺序的列表。如果这是一个布尔的list，必须匹配的长度的by。

​	***inplace***：**bool, default False**

​		如果为True，就地执行操作。

​	***kind*** ：**{‘quicksort’, ‘mergesort’, ‘heapsort’, ‘stable’}, default ‘quicksort’**

​		选择排序算法。有关更多信息，请参见[`numpy.sort()`](https://numpy.org/doc/stable/reference/generated/numpy.sort.html#numpy.sort) mergesort是唯一稳定的算法。对于DataFrames，仅在对单个列或标签进行排序时才应用此选项。

​	***na_position*** ：**{‘first’, ‘last’}, default ‘last’**

​		如果first将NaN放在开头; last将NaN放在最后。

​	***sort_remaining***：**bool, default True**

​		如果为True且按级别和索引排序是多层的，则在按指定级别排序后也按其他级别（按顺序）排序。

​	***ignore_index*** ：**bool, default False**

​		如果为True，则结果轴将标记为0、1，...，n-1。

​	***key***：**callable, optional**

​		如果不是None，则在排序之前将key函数应用于索引值。这类似于内建函数中的key参数sorted()，但值得注意的区别是此key函数应被向量化。它应期望 Index并返回具有相同形状的Index。对于MultiIndex输入，将按级别应用key。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sort_index.html)

#### **==DataFrame.swaplevel==**(i=- 2, j=- 1, axis=0)

###### MultiIndex 中的交换级别 i 和 j。默认情况是交换索引最里面的两个级别。

##### 参数设置：

​	**i**，**j**：**int or str**

​		要交换的索引的级别。可以将级别名称作为字符串传递。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		轴转换级别，在行方向交换“index”，在列方向交换1或“columns”。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.swaplevel.html)
