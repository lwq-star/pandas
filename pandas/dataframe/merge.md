#### **==DataFrame.combine==**(other, func, fill_value=None, overwrite=True)

###### 基于传递的函数执行与另一个DataFrame的逐列组合。使用func将DataFrame与其他 DataFrame 组合到按元素组合的列。生成的DataFrame的行索引和列索引将是两者的并集。

##### 参数设置：

​	***other***：**DataFrame**

​		要按列合并的DataFrame。

​	***func***：**function**

​		将两个系列作为输入并返回一个Series或一个标量的函数。用于逐列合并两个数据帧。

​	***fill_value***：**scalar value, default None**

​		在将任何列传递给合并函数之前填充NaN的值。

​	***overwrite***：**bool, default True**

​		如果为true，则自身中不存在于他人中的列将被NaNs覆盖。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.combine.html)

#### **==DataFrame.combine_first==**(other)

###### 用其他相同位置的值更新空元素。通过在一个DataFrame中使用来自其他DataFrame的非null值填充空值来组合两个DataFrame对象。生成的DataFrame的行索引和列索引将是两者的并集。

##### 参数设置：

​	***other***：**DataFrame**

​		提供了用于填充空值的DataFrame。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.combine_first.html)

#### ==**DataFrame.align**==(other, join='outer', axis=None, level=None, copy=True, fill_value=None, method=None, limit=None, fill_axis=0, broadcast_axis=None)

###### 使用指定的每个轴索引的连接方法，将轴上的两个对象对齐。

##### 参数设置：

​	***other***: **DataFrame or Series**

​	***join***: **{‘outer’, ‘inner’, ‘left’, ‘right’}, default ‘outer’**

​	***axis***：**allowed axis of the other object, default None**

​		对齐 index (0), columns (1), 或 both (None)

​	***level***：**int or level name, default None**

​		跨level广播，匹配传递的多索引level上的索引值

​	***copy***：**bool, default True**

​		始终返回新对象。如果copy = False并且不需要重建索引，则返回原始对象。

​	***fill_value***：**scalar, default np.NaN**

​		用于缺失值的值。默认为NaN，但可以是任何“兼容”值。

​	***method***: **{‘backfill’, ‘bfill’, ‘pad’, ‘ffill’, None}, default None**

​		用于填充reindexed系列孔的方法：

​			pad / ffill：将上次有效的观察传播到下一个有效性。

​			backfill / bfill：使用下一个有效观察来填补差距。

​	***limit***：**int, default None**

​		如果指定了method，则这是向前/向后填充的连续NaN值的最大数量。换句话说，如果存在超过此数量的连续NaN的间隙，则仅部分填充。如果未指定method，则这是沿整个轴填充NaN的最大条目数。如果不是None，则必须大于0。

​	***fill_axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		填充轴，方法和极限。

​	***broadcast_axis***：**{0 or ‘index’, 1 or ‘columns’}, default None**

​		如果对齐两个不同尺寸的对象，则沿此axis广播值

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.align.html)

#### **==DataFrame.append==**(other, ignore_index=False, verify_integrity=False, sort=False)

###### 在调用者的末尾追加其他行，返回一个新对象。不在调用者中的其他列将作为新列添加。

##### 参数设置：

​	***other***: **DataFrame or Series/dict-like object, or list of these**

​		要附加的数据。

​	***ignore_index***：**bool, default False**

​		如果为True，则不要使用索引标签。

​	***verify_integrity***：**bool, default False**

​		如果为True，在创建带有重复项的索引时引发ValueError。

​	***sort***：**bool, default False**

​		如果self和other的列没有对齐，则对列进行排序。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.append.html)

#### **==DataFrame.join==**(other, on=None, how='left', lsuffix='', rsuffix='', sort=False)

###### 在索引或键列上与其他DataFrame连接列。通过传递列表，有效地通过索引连接多个DataFrame对象。传递DataFrame对象列表时，不支持on，lsuffix和rsuffix选项。

##### 参数设置：

​	***other***：**DataFrame, Series, or list of DataFrame**

​		索引，应该类似于此列中的一列。如果传递了Series，则必须设置其name属性，并将其用作生成的连接DataFrame中的列名

​	***on***：**str, list of str, or array-like, optional**

​		调用者中的列或索引级别名称，用于连接其他索引，否则加入index-on-index。如果给定多个值，则另一个 DataFrame，必须具有MultiIndex。如果数组尚未包含在调用DataFrame中，则可以将数组作为连接键传递。像Excel VLOOKUP操作一样

​	***how***：**{‘left’, ‘right’, ‘outer’, ‘inner’}, default ‘left’**

​		如何处理这两个对象的操作。

​			1）left：使用调用框架的索引（如果指定了on，则使用列）

​			2）right：使用其他框架的索引

​			3）outer：调用框架索引的形式联合（或指定的列）与其他框架的索引，并按字典顺序对其进行排序

​			4）inner：调用框架索引（或指定的列）与其他框架索引的形式交集，保留调用框架的索引顺序

​	***lsuffix***：**str, default ‘’**

​		使用左框架重叠列的后缀

​	***rsuffix***：**str, default ‘’**

​		使用右框架重叠列的后缀

​	***sort***：**bool, default False**

​		通过联接键按词法对结果Dataframe进行排序。如果为False，则连接键的顺序取决于连接类型（关键字）

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.join.html)

#### **==DataFrame.merge==**(right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=False, suffixes=('_x', '_y'), copy=True, indicator=False, validate=None)

###### 用数据库样式的联接合并DataFrame或命名的Series对象。联接在列或索引上完成。如果在列上连接列，则DataFrame索引将被忽略。否则，如果在索引上连接索引或在一个或多个列上建立索引，则将传递索引。

##### 参数设置：

​	***right*** ： **DataFrame or named Series**

​		要合并的对象。

​	***how***：**{‘left’, ‘right’, ‘outer’, ‘inner’, ‘cross’}, default ‘inner’**

​		要执行的合并类型。

​			\1) left：仅使用左框架中的键，类似于SQL左外部联接；保留关键顺序

​			\2) right：仅使用右框架中的键，类似于SQL右外部联接；保留关键顺序

​			\3) outer：使用两个框架中键的并集，类似于SQL完全外部联接；按字典顺序排序键

​			\4) inner：使用两个框架中关键点的交集，类似于SQL内部联接；保留左键的顺序

​			5)cross：从两个框架中创建笛卡尔产品，保留左键的顺序。

​	***on***：**label or list**

​		要加入的列或索引级别名称。这些必须在两个DataFrame中都可以找到。如果on为None且未在索引上合并，则默认为两个DataFrame中列的交集。

​	***left_on***：**label or list, or array-like**

​		要在左侧DataFrame中加入的列或索引级别名称。也可以是左侧DataFrame长度的数组或数组列表。这些数组被视为列。

​	***right_on***：**label or list, or array-like**

​		要在右侧DataFrame中加入的列或索引级别名称。也可以是正确DataFrame长度的数组或数组列表。这些数组被视为列。

​	***left_index***：**bool, default False**

​		使用左侧DataFrame中的索引作为连接键。如果它是MultiIndex，则另一个DataFrame中的键数（索引或列数）必须与级别数匹配

​	***right_index***：**bool, default False**

​		使用右侧DataFrame中的索引作为连接键。与left_index相同的警告

​	***sort***：**bool, default False**

​		在结果DataFrame中按字典顺序对联接键进行排序。如果为False，则联接键的顺序取决于联接类型（how关键字）

​	***suffixes***：**list-like, default is (“_x”, “_y”)**

​		2个长度的序列（元组，列表等）。suffixes分别应用于左侧和右侧的重叠列名

​	***copy***：**bool, default True**

​		如果为False，请勿不必要地复制数据

​	***indicator***：**bool or str, default False**

​		如果为True，则在输出DataFrame中添加一列，称为“_merge”，其中包含有关每一行源的信息。如果为字符串，则将在每一行的源上带有信息的列,添加到输出DataFrame中，并将该列命名为字符串的值。信息列是分类类型的，对于其合并键仅出现在'left'DataFrame中的观测值，其值为“left_only”；对于其合并键仅出现在'right'。DataFrame中的观测值，其值为“right_only”，如果两者中都存在观察值的合并键。

​	***validate***：**str, optional**

​		如果指定，则检查合并是否为指定的类型。

​			“one_to_one”或“1:1”：检查合并键在左右数据集中是否唯一。

​			“one_to_many”或“1:m”：检查合并键在左数据集中是否唯一。

​			“many_to_one”或“m:1”：检查合并键在正确的数据集中是否唯一。

​			“many_to_many”或“m:m”：允许，但不进行检查。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html)

