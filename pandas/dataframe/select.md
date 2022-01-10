- [**==DataFrame.select_dtypes==**(include=None, exclude=None)](#dataframeselect_dtypesincludenone-excludenone)
    - [根据列类型返回DataFrame的列子集](#根据列类型返回dataframe的列子集)
  - [参数设置：](#参数设置)
  - [加注：](#加注)
  - [注意：](#注意)
- [官网](#官网)
- [**==DataFrame.head==**(n=5)](#dataframeheadn5)
    - [返回前 n 行。此函数根据位置返回对象的前 n 行。对于快速测试对象中是否包含正确类型的数据，它非常有用。对于 n 的负值，该函数返回除最后 n 行以外的所有行，等价于 df [ :-n ]。](#返回前-n-行此函数根据位置返回对象的前-n-行对于快速测试对象中是否包含正确类型的数据它非常有用对于-n-的负值该函数返回除最后-n-行以外的所有行等价于-df---n-)
  - [参数设置：](#参数设置-1)
- [官网](#官网-1)
- [==**DataFrame.at**==](#dataframeat)
    - [访问行/列标签对的单个值。与 loc 类似，它们都提供基于标签的查找。如果只需要在 DataFrame 或 Series 中获取或设置单个值，请使用 at。](#访问行列标签对的单个值与-loc-类似它们都提供基于标签的查找如果只需要在-dataframe-或-series-中获取或设置单个值请使用-at)
- [官网](#官网-2)
- [==**DataFrame.iat**==](#dataframeiat)
    - [按整数位置访问行/列对的单个值。与 iloc 类似，它们都提供基于整数的查找。如果只需要在 DataFrame 或 Series 中获取或设置单个值，请使用 iat。](#按整数位置访问行列对的单个值与-iloc-类似它们都提供基于整数的查找如果只需要在-dataframe-或-series-中获取或设置单个值请使用-iat)
- [官网](#官网-3)
- [==**DataFrame.loc**==](#dataframeloc)
    - [可以使用label值，但是也可以使用布尔值](#可以使用label值但是也可以使用布尔值)
- [官网](#官网-4)
- [==**DataFrame.iloc**==](#dataframeiloc)
    - [主要基于整数位置（从轴的0到长度为1），但也可以与布尔阵列一起使用。](#主要基于整数位置从轴的0到长度为1但也可以与布尔阵列一起使用)
- [官网](#官网-5)
- [**==DataFrame.insert==**(loc, column, value, allow_duplicates=False)](#dataframeinsertloc-column-value-allow_duplicatesfalse)
    - [在指定位置将列插入到 DataFrame 中。如果列已包含在 DataFrame 中，则引发 ValueError，除非 allow _ duplicates 设置为 True。](#在指定位置将列插入到-dataframe-中如果列已包含在-dataframe-中则引发-valueerror除非-allow-_-duplicates-设置为-true)
  - [参数设置：](#参数设置-2)
- [官网](#官网-6)
- [==**DataFrame.__iter__()**==](#dataframeiter)
- [==**DataFrame.items\iteritems()**==](#dataframeitemsiteritems)
    - [遍历(列名， Series )对。遍历DataFrame列，返回一个带有列名称和内容为Series的元组。](#遍历列名-series-对遍历dataframe列返回一个带有列名称和内容为series的元组)
- [官网](#官网-7)
- [==**DataFrame.keys()**==](#dataframekeys)
    - [返回Pandas 对象的“信息轴”。如果Pandas 对象是系列，则它返回索引。如果pandas对象是dataframe，则它返回列。](#返回pandas-对象的信息轴如果pandas-对象是系列则它返回索引如果pandas对象是dataframe则它返回列)
- [官网](#官网-8)
- [==**DataFrame.iterrows()**==](#dataframeiterrows)
    - [以(index，series)对的形式迭代 DataFrame 行](#以indexseries对的形式迭代-dataframe-行)
- [官网](#官网-9)
- [**==DataFrame.itertuples==**(index=True, name='Pandas')](#dataframeitertuplesindextrue-namepandas)
    - [将DataFrame行迭代为namedtuple。](#将dataframe行迭代为namedtuple)
  - [参数设置：](#参数设置-3)
- [官网](#官网-10)
- [**==DataFrame.pop==**(item)](#dataframepopitem)
    - [返回item并从frame中删除。如果找不到，会引发KeyError。](#返回item并从frame中删除如果找不到会引发keyerror)
  - [参数设置：](#参数设置-4)
- [官网](#官网-11)
- [**==DataFrame.tail==**(n=5)](#dataframetailn5)
    - [返回最后 n 行。此函数根据位置返回对象的最后 n 行。对于快速验证数据非常有用，例如，在排序或追加行之后。对于 n 的负值，该函数返回除前 n 行以外的所有行，等价于 df [ n: ]。](#返回最后-n-行此函数根据位置返回对象的最后-n-行对于快速验证数据非常有用例如在排序或追加行之后对于-n-的负值该函数返回除前-n-行以外的所有行等价于-df--n-)
  - [参数设置：](#参数设置-5)
- [官网](#官网-12)
- [**==DataFrame.xs==**(key, axis=0, level=None, drop_level=True)](#dataframexskey-axis0-levelnone-drop_leveltrue)
    - [返回Series/DataFrame的横截面(cross-section)。该方法使用一个关键参数来选择多索引特定级别的数据。](#返回seriesdataframe的横截面cross-section该方法使用一个关键参数来选择多索引特定级别的数据)
  - [参数设置：](#参数设置-6)
  - [注意：](#注意-1)
- [官网](#官网-13)
- [**==DataFrame.get==**(key, default=None)](#dataframegetkey-defaultnone)
    - [从给定键的对象中获取项目。键可以是一个或多个DataFrame 列。如果找不到，它将返回默认值。](#从给定键的对象中获取项目键可以是一个或多个dataframe-列如果找不到它将返回默认值)
  - [参数设置：](#参数设置-7)
- [官网](#官网-14)
- [**==DataFrame.filter==**(items=None, like=None, regex=None, axis=None)](#dataframefilteritemsnone-likenone-regexnone-axisnone)
    - [根据指定索引中的标签对数据框的行或列进行子集设置。请注意，此例程不会在其内容上过滤数据框。过滤器将应用于索引标签。items，like和regex参数执行相互排斥。axis默认为使用[]建立索引时使用的信息轴。](#根据指定索引中的标签对数据框的行或列进行子集设置请注意此例程不会在其内容上过滤数据框过滤器将应用于索引标签itemslike和regex参数执行相互排斥axis默认为使用建立索引时使用的信息轴)
  - [参数设置：](#参数设置-8)
- [官网](#官网-15)
- [**==DataFrame.sample==**(n=None, frac=None, replace=False, weights=None, random_state=None, axis=None, ignore_index=False)](#dataframesamplennone-fracnone-replacefalse-weightsnone-random_statenone-axisnone-ignore_indexfalse)
    - [从对象轴返回随机的项目样本。您可以使用random_state来实现重现性。如果 frac > 1，则replace应设置为 True。](#从对象轴返回随机的项目样本您可以使用random_state来实现重现性如果-frac--1则replace应设置为-true)
  - [参数设置：](#参数设置-9)
- [官网](#官网-16)
- [**==DataFrame.take==**(indices, axis=0, is_copy=None, **kwargs)](#dataframetakeindices-axis0-is_copynone-kwargs)
    - [沿着坐标轴返回给定位置索引中的元素。这意味着我们没有根据对象的索引属性中的实际值进行索引。我们根据元素在对象中的实际位置建立索引。](#沿着坐标轴返回给定位置索引中的元素这意味着我们没有根据对象的索引属性中的实际值进行索引我们根据元素在对象中的实际位置建立索引)
  - [参数设置：](#参数设置-10)
- [官网](#官网-17)
- [**==DataFrame.truncate==**(before=None, after=None, axis=None, copy=True)](#dataframetruncatebeforenone-afternone-axisnone-copytrue)
    - [在某个索引值之前和之后Truncate Series或DataFrame。这是基于高于或低于某些阈值的索引值，进行布尔索引的有用捷径。如果被truncate的索引仅包含日期时间值，则 可以将字符串之前和之后指定为字符串，而不是时间戳。](#在某个索引值之前和之后truncate-series或dataframe这是基于高于或低于某些阈值的索引值进行布尔索引的有用捷径如果被truncate的索引仅包含日期时间值则-可以将字符串之前和之后指定为字符串而不是时间戳)
  - [参数设置：](#参数设置-11)
- [官网](#官网-18)
- [**==DataFrame.nlargest\nsmallest==**(n, columns, keep='first')](#dataframenlargestnsmallestn-columns-keepfirst)
    - [返回按列降序\升序排列的前n行。以降序升序返回column中具有最大值的前n行。未指定的列也将返回，但不用于排序。此方法等效于 ，但性能更高。df.sort_values(columns, ascending=False\True).head(n)](#返回按列降序升序排列的前n行以降序升序返回column中具有最大值的前n行未指定的列也将返回但不用于排序此方法等效于-但性能更高dfsort_valuescolumns-ascendingfalsetrueheadn)
  - [参数设置：](#参数设置-12)
- [官网](#官网-19)

#### **==DataFrame.select_dtypes==**(include=None, exclude=None)

###### 根据列类型返回DataFrame的列子集

##### 参数设置：

​	***include, exclude***：**scalar or list-like**

​		选择要包含/排除的类型或字符串。必须至少提供其中一个参数。

##### 加注：

​	ValueError：

​		如果include和exclude都为空

​		如果包含和排除有重叠的元素

​		如果传入任何类型的字符串

##### 注意：

​	要选择所有的数字类型，请使用np.number或'number'

​	要选择字符串，您必须使用object类型，但是请注意，这将返回所有object类型列

​	请参见[numpy dtype层次结构](https://numpy.org/doc/stable/reference/arrays.scalars.html)

​	要选择 datetimes，使用  np.datetime64, 'datetime' or 'datetime64'

​	要选择 timedeltas，使用 np.timedelta64, 'timedelta' or 'timedelta64'

​	要选择Pandas categorical类型，请使用 'category'

​	要选择Pandas datetimetz 类型，请使用'datetimetz' 或 'datetime64[ns, tz]'

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.select_dtypes.html)

#### **==DataFrame.head==**(n=5)

###### 返回前 n 行。此函数根据位置返回对象的前 n 行。对于快速测试对象中是否包含正确类型的数据，它非常有用。对于 n 的负值，该函数返回除最后 n 行以外的所有行，等价于 df [ :-n ]。

##### 参数设置：

​	***n***：要选择的行数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html)

#### ==**DataFrame.at**==

###### 访问行/列标签对的单个值。与 loc 类似，它们都提供基于标签的查找。如果只需要在 DataFrame 或 Series 中获取或设置单个值，请使用 at。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.at.html)

#### ==**DataFrame.iat**==

###### 按整数位置访问行/列对的单个值。与 iloc 类似，它们都提供基于整数的查找。如果只需要在 DataFrame 或 Series 中获取或设置单个值，请使用 iat。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iat.html)

#### ==**DataFrame.loc**==

###### 可以使用label值，但是也可以使用布尔值

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html)

#### ==**DataFrame.iloc**==

###### 主要基于整数位置（从轴的0到长度为1），但也可以与布尔阵列一起使用。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iloc.html)

#### **==DataFrame.insert==**(loc, column, value, allow_duplicates=False)

###### 在指定位置将列插入到 DataFrame 中。如果列已包含在 DataFrame 中，则引发 ValueError，除非 allow _ duplicates 设置为 True。

##### 参数设置：

​	***loc***：int

​		插入索引。必须符合0 < = loc < = len (列)。

​	***column***：**str, number, or hashable object**

​		插入列的标签。

​	***value***：**int, Series, or array-like**

​		要插入的值，整数、Series或者数组型数据

​	***allow_duplicates***：**bool, optional**

​		如果dataframe中已经存在某列，将allow_duplicates置为true才可以将指定得列插入。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.insert.html)

#### ==**DataFrame.__iter__()**==

创建一个 Python iterator 在列索引轴上迭代的对象。

#### ==**DataFrame.items\iteritems()**==

###### 遍历(列名， Series )对。遍历DataFrame列，返回一个带有列名称和内容为Series的元组。

return：

label：要迭代的DataFrame的列名。

content：属于每个标签的列条目(作为Series )。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.items.html)

#### ==**DataFrame.keys()**==

###### 返回Pandas 对象的“信息轴”。如果Pandas 对象是系列，则它返回索引。如果pandas对象是dataframe，则它返回列。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.keys.html)

#### ==**DataFrame.iterrows()**==

###### 以(index，series)对的形式迭代 DataFrame 行

return:

index：行的索引。一个元组，用于多级索引。

data：行的数据作为series。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iterrows.html)

#### **==DataFrame.itertuples==**(index=True, name='Pandas')

###### 将DataFrame行迭代为namedtuple。

##### 参数设置：

​	***index***：**bool, default True**

​		如果为True，则将索引作为元组的第一个元素返回。

​	***name***：**str or None, default “Pandas”**

​		返回的namedtuple的名称，或者返回None以返回常规元组。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.itertuples.html)

#### **==DataFrame.pop==**(item)

###### 返回item并从frame中删除。如果找不到，会引发KeyError。

##### 参数设置：

​	***item***：要pop出的列的标签。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pop.html)

#### **==DataFrame.tail==**(n=5)

###### 返回最后 n 行。此函数根据位置返回对象的最后 n 行。对于快速验证数据非常有用，例如，在排序或追加行之后。对于 n 的负值，该函数返回除前 n 行以外的所有行，等价于 df [ n: ]。

##### 参数设置：

​	***n***：要选择的行数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tail.html)

#### **==DataFrame.xs==**(key, axis=0, level=None, drop_level=True)

###### 返回Series/DataFrame的横截面(cross-section)。该方法使用一个关键参数来选择多索引特定级别的数据。

##### 参数设置：

​	***key***: label 或 tuple of label。

​		label包含在索引中，或部分包含在多索引中。

​	***axis***: {0 或‘index’, 1 或‘columns’}, 默认 0。

​		轴上检索横截面(cross-section)。

​	***level***: **object, defaults to first n levels (n=1 or len(key))**。

​		如果key部分包含在多索引中，请指示使用了哪些级别。级别可以通过label 或 position来引用。

​	***drop_level***: **bool, default True**。

​		如果为False，返回与自己级别相同的对象。

##### 注意：

Xs 不能用于设置值。MultiIndex slicker 是获取/设置任何级别上的值的通用方法。它是 xs 功能的超集，请参见 [MultiIndex Slicers](https://pandas.pydata.org/docs/user_guide/advanced.html#advanced-mi-slicers).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.xs.html)

#### **==DataFrame.get==**(key, default=None)

###### 从给定键的对象中获取项目。键可以是一个或多个DataFrame 列。如果找不到，它将返回默认值。

##### 参数设置：

​	***key***: **object**

​		对象中包含的项目类型

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.get.html)

#### **==DataFrame.filter==**(items=None, like=None, regex=None, axis=None)

###### 根据指定索引中的标签对数据框的行或列进行子集设置。请注意，此例程不会在其内容上过滤数据框。过滤器将应用于索引标签。items，like和regex参数执行相互排斥。axis默认为使用[]建立索引时使用的信息轴。

##### 参数设置：

​	***items*** ： **list-like**

​		保持标签中轴的位置。

​	***like*** ： **str**

​		将标签与“ like in label = = True”的轴保持一致。

​	***regex*** ：**str (regular expression)**

​		保留 re.search (regex，label) = = True 的轴上的标签。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’, None}, default None**

​		默认情况下，这是信息轴，‘index’用于Series，‘columns’用于DataFrame。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.filter.html)

#### **==DataFrame.sample==**(n=None, frac=None, replace=False, weights=None, random_state=None, axis=None, ignore_index=False)

###### 从对象轴返回随机的项目样本。您可以使用random_state来实现重现性。如果 frac > 1，则replace应设置为 True。

##### 参数设置：

​	**n**：**int, optional**

​		从轴返回的项目数。 不能与frac一起使用。 如果frac = None，则Default = 1。

​	**frac**：**float, optional**

​		要返回的轴项的Fraction。不能与n一起使用。

​	**replace**：**bool, default False**

​		允许或不允许对同一行进行多次抽样。

​	**weights**：**str or ndarray-like, optional**

​		默认的‘None’将导致相等的概率权重。如果传递了一个Series，将与目标对象上的索引对齐。权重中未被采样对象发现的索引值将被忽略，权重中未被采样对象的索引值将被赋值为零。如果在DataFrame上调用，将在axis = 0时接受列的名称。除非权值是一个Series，否则权值必须与被采样的轴线长度相同。如果权重的和不是1，它们将被规范化为和为1。weights列中缺失的值将被视为零。不允许无限值。

​	**random_state**：**int, array-like, BitGenerator, np.random.RandomState, optional**

​		如果int，array-like，或BitGenerator (NumPy>=1.17)，种子为随机数生成器，如果np.random。随机状态，用作numpy随机状态对象。

​	**axis**：**{0 or ‘index’, 1 or ‘columns’, None}, default None**

​		轴采样。接受轴编号或名称。默认为给定数据类型的统计轴（0 for series和dataframes）。

​	**ignore_index**：**bool, default False**

​		如果为true，则结果索引将标记为0,1，...，n - 1。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sample.html)

#### **==DataFrame.take==**(indices, axis=0, is_copy=None, **kwargs)

###### 沿着坐标轴返回给定位置索引中的元素。这意味着我们没有根据对象的索引属性中的实际值进行索引。我们根据元素在对象中的实际位置建立索引。

##### 参数设置：

​	**indices**：**array-like**

​		一个整数数组，指示要take的位置。

​	**axis**：**{0 or ‘index’, 1 or ‘columns’, None}, default 0**

​		选择元素的轴。0表示选择行，1表示选择列。

​	***\*kwargs**：与兼容numpy.take()。对输出没有影响。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.take.html)

#### **==DataFrame.truncate==**(before=None, after=None, axis=None, copy=True)

###### 在某个索引值之前和之后Truncate Series或DataFrame。这是基于高于或低于某些阈值的索引值，进行布尔索引的有用捷径。如果被truncate的索引仅包含日期时间值，则 可以将字符串之前和之后指定为字符串，而不是时间戳。

##### 参数设置：

​	**before** ：**date, str, int**

​		Truncate此索引值之前的所有行。

​	**after** ：**date, str, int**

​		Truncate此索引值之后的所有行。

​	**axis** ：**{0 or ‘index’, 1 or ‘columns’}, optional**

​		Truncate轴。默认情况下Truncate索引（行）。

​	**copy** ：**bool, default is True**

​		返回truncated部分的副本。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.truncate.html)

#### **==DataFrame.nlargest\nsmallest==**(n, columns, keep='first')

###### 返回按列降序\升序排列的前n行。以降序升序返回column中具有最大值的前n行。未指定的列也将返回，但不用于排序。此方法等效于 ，但性能更高。df.sort_values(columns, ascending=False\True).head(n)

##### 参数设置：

​	**n**：**int**

​		要返回的行数。

​	**columns**：**label or list of labels**

​		要排序的列标签。

​	**keep** ：**{‘first’, ‘last’, ‘all’}, default ‘first’**

​		其中有重复的值:

​			\1) first：优先处理第一次出现的事件

​			\2) last：确定最后出现的优先顺序

​			\3) all: 请勿丢弃任何重复项，即使这意味着选择n个以上的项目。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.nlargest.html)

