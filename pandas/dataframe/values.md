#### ==**DataFrame.values**==

###### 返回 DataFrame 的 Numpy 表示形式。只返回 DataFrame 中的值，轴标签将被删除。

##### 结果：

​	**numpy.ndarray**：dataframe的值。

#### 注意：

Dtype 将是一个较低的公分母 dtype (隐式上传) ; 也就是说，如果 dtype (甚至是数字类型)是混合的，那么将选择容纳所有类型的 dtype。如果你不是在处理积木，请小心使用	它。例如:。如果 dtype 是 float16和 float32，则 dtype 将向上转换为 float32。如果 dtype 是 int32和 uint8，那么 dtype 将向上转换为 int32。通过 [numpy.find_common_type()](https://numpy.org/doc/stable/reference/generated/numpy.find_common_type.html#numpy.find_common_type) 转化，将 int64和 uint64混合将导致 float64 dtype。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.values.html)

#### ==**DataFrame.empty**==

###### 指示 DataFrame 是否为空。如果 DataFrame 完全为空(没有项) ，则为 True，这意味着任何轴的长度为0。如果 DataFrame 只包含 nan，那么它仍然不被认为是空的。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.empty.html)

#### **==DataFrame.copy==**(deep=True)

###### 复制此对象的索引和数据。

当deep=True（默认）时，将使用调用对象的数据和索引的副本创建新对象。对副本的数据或索引的修改不会反映在原始对象中（请参阅下面的注释）。

当deep=False，将创建一个新对象而不复制调用对象的数据或索引（仅复制对数据和索引的引用）。对原始数据的任何更改都将反映在浅层副本中（反之亦然）。

##### 参数设置：

​	***deep***：**bool, default True**

​		制作深度拷贝，包括数据和索引的副本。使用 deep = False 时，索引和数据都不会被复制。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.copy.html)

#### **==DataFrame.bool==()**

返回单个元素 Series 或 DataFrame 的 bool。这必须是一个布尔标量值，True 或 False。如果 Series 或 DataFrame 没有正好包含1个元素，或者该元素不是 boolean (整数值0和1也会引发异常) ，则会引发 ValueError。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.bool.html)

#### **==DataFrame.isin==**(values)

###### 检查 DataFrame 中的每个元素是否包含输入的 values 中指定的值。返回布尔型的 DataFrame。

##### 参数设置：

​	***values***：**iterable, Series, DataFrame or dict**

​		只有当所有标签都匹配时，结果才是真实的。如果值是一个系列，那么它就是索引。如果值是 dict，那么键必须是列名，而列名必须匹配。如果值是 DataFrame，则索引标签和列标签必须匹配。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.isin.html)

#### **==DataFrame.where\mask==**(cond, other=nan, inplace=False, axis=None, level=None, errors='raise', try_cast=NoDefault.no_default)

###### 替换条件为 False\True 的值。

##### 参数设置：

​	***cond***：**bool Series/DataFrame, array-like, or callable**

​		当cond为True\False时，保持原始值。当为False\True时，用other的相应值替换。如果cond是可调用的，它将根据Series/DataFrame计算，并且应该返回boolean Series/DataFrame或array。可调用对象不能更改输入Series/DataFrame(尽管panda不检查它)。

​	***other***：**scalar, Series/DataFrame, or callable**

​		cond为假\真的条目被替换为other的相应值。如果其他变量是可调用的，它将根据Series/DataFrame计算，并且应该返回scalar或Series/DataFrame。可调用对象不能更改输入Series/DataFrame(尽管panda不检查它)。

​	***inplace***：**bool, default False**

​		是否对数据执行适当的操作。

​	***axis***：**int, default None**

​		如有需要，调整axis。

​	**level**：**int, default None**

​		如果需要对齐level。

​	***errors***：**str, {‘raise’, ‘ignore’}, default ‘raise’**

​		请注意，目前这个参数不会影响结果，并且总是将其强制为合适的dtype。

1) ‘raise’ : 允许引发异常。

2) ‘ignore’ : 抑制异常。错误时返回原始对象。

##### 注意：

Where 方法是 if-then 习惯用法的应用程序。对于调用 DataFrame 的每个元素，如果 cond 为 True\False，则使用元素; 否则使用来自 dataframeother 的对应元素。有关详细信息和示例，请参阅文档在[indexing](https://pandas.pydata.org/docs/user_guide/indexing.html#indexing-where-mask)中的位置。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.where.html)

#### **==DataFrame.query==**(expr, inplace=False, **kwargs)

###### 使用布尔表达式查询 DataFrame 的列。

##### 参数设置：

​	***expr***：**str**

​		要评估的查询字符串。您可以在环境中引用变量，方法是在变量前加上'@'字符，例如 。@a + b您可以通过在反引号中将空格或运算符括起来来引用它们。这样，您还可以转义以数字开头或Python关键字的名称。基本上是无效的Python标识符。有关更多详细信息，请参见注释。例如，如果你的一列叫做a a ，你想把它和b相加，你的查询应该是' a a ' + b。

​	***inplace***：**bool**

​		查询是应该修改数据还是返回修改后的副本。

​	***kwargs*：

​		有关 DataFrame.query ()接受的关键字参数的详细信息，请参阅 [eval()](https://pandas.pydata.org/docs/reference/api/pandas.eval.html#pandas.eval) 文档。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.query.html)

#### **==DataFrame.all==**(axis=0, bool_only=None, skipna=True, level=None, **kwargs)

###### 返回是否所有元素都是 True，可能超过一个轴。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’, None}, default 0**

​		指出哪个轴或哪个轴应该减少。0 / ‘index’ : 减少索引，返回索引为原始列标签的Series。1 / ‘columns’ : 减少列，返回一个索引为原始索引的Series。None : 减少所有轴，返回一个标量。

​	***bool_only***：**bool, default None**

​		只包含布尔列。如果没有，将尝试使用一切，然后只使用布尔数据。不适用于Series。

​	***skipna***：**bool, default True**

​		排除NA/null值。如果整个row/column为NA，并且skipna为True，那么对于空row/column，结果将为True。如果skipna是False，那么NA就被当作True，因为它们不等于零。

​	***level***：**int or level name, default None**

​		如果轴是一个多索引(层次结构)，则沿着特定的level进行计数，并折叠成一个Series。

​	***\*kwargs**：**any, default None**

​		附加关键字没有效果，但是可以接受与NumPy兼容。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.all.html)

#### ==**DataFrame.any**==(axis=0, bool_only=None, skipna=True, level=None, **kwargs)

###### 返回是否至少一个元素为True，可能超过一个轴。

参数与all相同

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.any.html)

#### **==DataFrame.clip==**(lower=None, upper=None, axis=None, inplace=False, *args, **kwargs)

###### 在输入阈值处修剪值。将边界外的值指定给边界值。阈值可以是奇异值或数组，并且在后一种情况下，剪切在指定轴中以元素方式执行。

##### 参数设置：

​	***lower***：**float or array-like, default None**

​		最小阈值。低于此阈值的所有值都将设置为它。

​	***upper***：**float or array-like, default None**

​		最大阈值。高于此阈值的所有值都将设置为它。

​	***axis***：**int or str axis name, optional**

​		沿给定轴将对象与下部和上部对齐。

​	***inplace***：**bool, default False**

​		是否对数据执行操作。

​	***args****， **kwargs**：其他关键字没有效果，但可以接受与numpy的兼容性。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.clip.html)

#### **==DataFrame.diff==**(periods=1, axis=0)

###### 第一个离散的元素差异。计算DataFrame元素与DataFrame中另一个元素的差异（默认值是前一行的同一列中的元素）。

##### 参数设置：

​	***periods***：**int, default 1**

​		用于计算差异的周期，接受负值。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		区分行（0）或列（1）。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.diff.html)

#### ==**DataFrame.eval**==(expr, inplace=False, **kwargs)

###### 评估描述DataFrame列上的操作的字符串。仅在列上操作，而不在特定的行或元素上操作。数据越大，表达式越大，使用eval().

##### 参数设置：

​	***expr***：**str**

​		要评估的表达式字符串。

​	***inplace***：**bool, default False**

​		如果表达式包含一个赋值，则是否就地执行操作并更改现有的DataFrame。否则，将返回一个新的DataFrame。

​	**kwargs**：有关eval()接受的关键字参数的完整详细信息， 请参见文档 [`query()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.query.html#pandas.DataFrame.query)。

这些操作由以下支持[pandas.eval()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.eval.html#pandas.eval)：

- 除了左移     ( <<) 和右移 ( >>) 运算符之外的算术运算，例如，df + 2 * pi / s ** 4 % 42 - the_golden_ratio
- 比较操作，包括链式比较，例如， 2 < df < df2
- 布尔运算，例如， df < df2 and df3 < df4 or not df_bool
- list和tuple文字，例如，或[1, 2](1, 2)
- 属性访问，例如， df.a
- 下标表达式，例如， df[0]
- 简单的变量评估，例如，pd.eval("df")（这不是很有用）
- 数学函数：sin, cos, exp, log, expm1, log1p, sqrt, sinh, cosh, tanh, arcsin, arccos, arctan, arccosh, arcsinh, arctanh, abs,arctan2和log10。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.eval.html)

#### **==DataFrame.rank==**(axis=0, method='average', numeric_only=None, na_option='keep', ascending=True, pct=False)

###### 计算沿轴的数值数据等级（1到n）。默认情况下，为相等的值分配一个等级，该等级是这些值的等级的平均值。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		直接排名的索引。

​	***method***：**{‘average’, ‘min’, ‘max’, ‘first’, ‘dense’}, default ‘average’**

​		如何对具有相同值（即ties）的记录组进行排名：

​			\1) average：组的平均等级

​			\2) min：组中最低的排名

​			\3) max：组中最高等级

​			\4) first : 按排列顺序排列，依次排列

​			\5) dense：类似于 ‘min’，但组之间的排名始终提高1

​	***numeric_only***：**bool, optional**

​		对于DataFrame对象，如果设置为True，则仅对数字列进行排名。

​	***na_option***：**{‘keep’, ‘top’, ‘bottom’}, default ‘keep’**

​		如何对NaN值进行排名：

​			\1) keep：将NaN等级分配给NaN值

​			\2) top：如果升序，则将最小等级分配给NaN值

​			\3) bottom：如果升序，则将最高等级分配给NaN值。

​	***ascending***：**bool, default True**

​		元素是否应该按升序排列。

​	***pct***：**bool, default False**

​		是否以百分比形式显示返回的排名。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rank.html)

#### **==DataFrame.round==**(decimals=0, *args, **kwargs)

###### 将 DataFrame 舍入到可变的小数位数。

##### 参数设置：

​	***decimals***：**int, dict, Series**

​		将每一列四舍五入的小数位数。如果给定了int，则将每列四舍五入到相同的位置。否则，dict和Series将四舍五入到可变数位。如果小数点是类似于骰子的，则列名应该在键中;如果小数是Series，则应该在索引中。任何未包含在小数中的列将保留原样。不属于输入列的小数元素将被忽略。

​	***args**：其他关键字没有影响，但可以接受与numpy的兼容性。

​	***\*kwargs**：其他关键字没有影响，但可以接受与numpy的兼容性。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.round.html)

#### **==DataFrame.nunique==**(axis=0, dropna=True)

###### 计算指定轴上不同元素的数目。返回具有个不同元素的序列。可以忽略 NaN 值。

##### 参数设置：

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要使用的轴。行为0或'index'，列为1或'columns'。

​	***dropna***：**bool, default True**

​		是否在计数中包括NaN。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.nunique.html)

#### **==DataFrame.value_counts==**(subset=None, normalize=False, sort=True, ascending=False, dropna=True)

###### 返回一个包含DataFrame中唯一行数的Series

##### 参数设置：

​	***subset***：**list-like, optional**

​		计算唯一组合时要使用的列。

​	***normalize***：**bool, default False**

​		返回比例而不是频率。

​	***sort***：**bool, default True**

​		按频率排序。

​	***ascending***：**bool, default False**

​		升序排列。

​	***dropna***：**bool, default True**

​		不要包括包含 NA 值的行计数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.value_counts.html)

#### **==DataFrame.drop==**(labels=None, axis=0, index=None, columns=None, level=None, inplace=False, errors='raise')

###### 从行或列中删除指定的标签。通过指定标签名称和相应的轴，或者直接指定索引或列名称，来移除行或列。当使用多索引时，可以通过指定级别删除不同级别的标签。

##### 参数设置：

​	***labels***：**single label or list-like**

​		要删除的索引或列标签。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		是否从索引（0或'索引'）或列（1或'列'）中删除标签。

​	***index***：**single label or list-like**

​		单个标签或类似列表。指定轴的替代方法（labels, axis=0 相当于index=labels）。

​	***columns***：**single label or list-like**

​		单个标签或类似列表。指定轴的替代方法（ labels, axis=1相当于columns=labels）。

​	***level***：**int or level name, optional**

​		对于MultiIndex，将从中删除标签的级别。

​	***inplace***：**bool, default False**

​		如果为True，则执行就地操作并返回None。

​	***errors***：**{‘ignore’, ‘raise’}, default ‘raise’**

​		如果“忽略”，则禁止错误，仅删除现有标签。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html)

#### **==DataFrame.drop_duplicates==**(subset=None, keep='first', inplace=False, ignore_index=False)

###### 返回删除了重复行的DataFrame，可选择仅考虑某些列。包括时间索引在内的索引将被忽略。

##### 参数设置：

​	***subset***：**column label or sequence of labels, optional**

​		仅考虑用于标识重复项的某些列，默认情况下使用所有列

​	***keep***： **{‘first’, ‘last’, False}, default ‘first’**

  	 first ：删除第一次出现的重复项。
  	
  	 last ：删除重复项，除了最后一次出现。
  	
  	 False：删除所有重复项。

​	***inplace*：**bool, default False

​		是否删除重复项或返回副本

​	**ignore_index**：bool, default False

​		如果为true，则结果轴将标记为0,1，...，n - 1。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop_duplicates.html)

#### **==DataFrame.duplicated==**(subset=None, keep='first')

###### 返回表示重复行的布尔Series，可以选择仅考虑某些列。

##### 参数设置：

​	***subset*** ： **column label or sequence of labels, optional**

​		仅考虑某些列来标识重复项，默认情况下使用所有列

​	***keep*** ：**{‘first’, ‘last’, False}, default ‘first’**

  	first：将重复项标记True为第一次出现的除外。
  	
  	last：将重复项标记True为最后一次除外。
  	
  	False：将所有重复项标记为True。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.duplicated.html)

#### **==DataFrame.equals==**(other)

###### 测试两个对象是否包含相同的元素。此功能允许将两个Series或DataFrame相互比较，以查看它们是否具有相同的形状和元素。相同位置的NaN被认为是相等的。列标题不必具有相同的类型，但是列中的元素必须具有相同的dtype。

##### 参数设置：

​	***other***：**Series or DataFrame**

​		其他Series或DataFrame与第一个进行比较。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.equals.html)

#### **==DataFrame.replace==**(to_replace=None, value=None, inplace=False, limit=None, regex=False, method='pad')

###### 将to_replace中给出的值替换为value。DataFrame的值被动态替换为其他值。这与使用.loc或.iloc进行更新不同，后者要求您指定要使用某个值进行更新的位置。

##### 参数设置：

​	***to_replace*** : **str, regex, list, dict, Series, int, float, or None**

​		如何找到将要被替换的值。

​			numeric, str 或 regex:

​				1）numeric: 等于to_replace的数值将被替换为value

​				2）str: 完全匹配to_replace的字符串将被替换为值

​				3）regex: 匹配to_replace的正则表达式将被替换为值

​			str, regex, 或 numeric的list:

​				1）首先，如果to_replace和value都是列表，那么它们的长度必须相同。

​				2）其次，如果regex=True，那么两个列表中的所有字符串都将被解释为regex，否则它们将直接匹配。这对值没有太大影响，因为您只能使用几种可能的替代正则表达式。

​				3）str、regex和numeric规则同样适用。

​			dict : 

​				1）dict可用于为不同的现有值指定不同的替换值。例如，{'a': 'b'， 'y': 'z'}将值'a'替换为'b'，将值'y'替换为'z'。要以这种方式使用dict, value参数应该为None。

​				2）对于数据格式，dict可以指定在不同的列中替换不同的值。例如，{'a': 1， 'b': 'z'}查找列'a'中的值1和列'b'中的值'z'，并用value中指定的值替换这些值。在这种情况下，value参数不应该是None。除了指定要搜索的列之外，您可以将此看作传递两个列表的特殊情况。

​				3）对于一个DataFrame嵌套字典.例如，{'a': {'b': np.nan}}，读取如下:在'a'列中查找值'b'，并将其替换为NaN。要以这种方式使用嵌套的dict, value参数应该为None。您也可以嵌套正则表达式。注意列名(嵌套字典中的顶级字典键)不能是正则表达式。

​			None:

​				1）这意味着regex参数必须是字符串、编译regex或list、dict、ndarray或这类元素的Series。如果值也是None，那么这必须是嵌套字典或序列。请参阅示例部分以获得这些示例。

​	***value*** : **scalar, dict, list, str, regex, default None**

​		以替换与to_replace匹配的任何值。对于DataFrame，可以使用一组值来指定为每个列使用哪个值(不属于该数据格式的列将不会被填充)。这些对象的正则表达式、字符串和列表或字典也是允许的。

​	***inplace*** :**bool, default False**

​		如果为真，则执行原位操作并返回 None。

​	***limit*** : **int, default None**

​		向前或向后填充的最大尺寸gap。

​	***regex*** :**bool or same types as** to_replace**, default False**

​		是否将to_replace和/或value解释为正则表达式。如果这是True，那么to_replace必须是一个字符串。也可以是正则表达式或正则表达式的列表、dict或数组，在这种情况下to_replace必须为None。

​	***method* :{‘pad’, ‘ffill’, ‘bfill’, None}**

​		当用于替换时，当to_replace是标量时，列表或元组，值为None时使用的方法。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.replace.html)

#### **==DataFrame.sort_values==**(by, axis=0, ascending=True, inplace=False, kind='quicksort', na_position='last', ignore_index=False, key=None)

###### 沿任一轴按values排序。

##### 参数设置：

​	***by***：**str or list of str**

​		要排序的名称或名称列表。

​			\1) 如果axis是0或'index'，那么by可能包含索引级别and/or列标签。

​			\2) 如果axis是1或'columns'，那么by可能包含列级别and/or索引标签。

​	***axis*** ：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要排序的轴(axis)。

​	***ascending***：**bool or list of bool, default True**

​		升序和降序排序。指定多个排序顺序的列表。如果这是一个布尔的list，必须匹配的长度的by。

​	***inplace***：**bool, default False**

​		如果为True，就地执行操作。

​	***kind*** ：**{‘quicksort’, ‘mergesort’, ‘heapsort’, ‘stable’}, default ‘quicksort’**

​		选择排序算法。有关更多信息，请参见[`numpy.sort()`](https://numpy.org/doc/stable/reference/generated/numpy.sort.html#numpy.sort)。 mergesort是唯一稳定的算法。对于DataFrames，仅在对单个列或标签进行排序时才应用此选项。

​	***na_position*** ：**{‘first’, ‘last’}, default ‘last’**

​		如果first将NaN放在开头; last将NaN放在最后。

​	***ignore_index*** ：**bool, default False**

​		如果为True，则结果轴将标记为0、1，...，n-1。

​	***key***：**callable, optional**

​		在排序之前，将键函数应用于这些值。这类似于内建函数中的key参数sorted()，但值得注意的区别是此key函数应被向量化。它应该期望Series并返回与输入形状相同的Series。它将应用于by独立的每一列。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sort_values.html)

#### **==DataFrame.update==**(other, join='left', overwrite=True, filter_func=None, errors='ignore')

###### 使用来自另一个DataFrame的非NA值进行适当的修改。在索引上对齐，没有返回值。

##### 参数设置：

​	**other**：**DataFrame, or object coercible into a DataFrame**

​		应该至少有一个与原始DataFrame匹配的index/column标签。如果传递了一个Series，则必须设置它的name属性，并将其用作列名，以便与原始的DataFrame保持一致。

​	**join**：**{‘left’}, default ‘left’**

​		只实现left join，保留原始对象的索引和列。

​	**overwrite**：**bool, default True**

​		如何处理重复键的非NA值：

​			\1) True：用其他 DataFrame的值覆盖原始数据的值。

​			\2) False：仅更新原始DataFrame中NA的值。

​	**filter_func**：**callable(1d-array) -> bool 1d-array, optional**

​		可以选择替换NA以外的值。对于应该更新的值返回True。

​	**errors**：**{‘raise’, ‘ignore’}, default ‘ignore’**

​		如果为'raise'，则当DataFrame和其他两者在同一位置包含非NA数据时，将引发ValueError 。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.update.html)

#### **==DataFrame.first_valid_index\last_valid_index==**()

###### 返回数据帧中第一个\最后一个非NA /空值的索引。如果是Pandas 系列，则返回第一个非NA /空索引。对于pandas Dataframe，将返回该索引，该索引的行甚至具有单个非NA /null值。如果所有元素都不为NA /null，则返回None。对于空的DataFrame也返回None

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.first_valid_index.html)

