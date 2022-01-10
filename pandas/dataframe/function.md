#### **==DataFrame.apply==**(func, axis=0, raw=False, result_type=None, args=(), **kwargs)

###### 沿着DataFrame的轴应用一个函数。传递给函数的对象是Series对象，其索引要么是DataFrame的索引(轴=0)，要么是DataFrame的列(axis=1)。默认情况下(result_type=None)，最终的返回类型是从应用函数的返回类型推断出来的。否则，它取决于result_type参数。

##### 参数设置：

​	***func***: function

​		作用于每一列或行。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		函数所应用的轴。0 或‘index’: 对每一列应用函数。1 或‘columns’: 对每一行应用函数。

​	***raw***：**bool, default False**

​		确定行或列是否作为 Series 对象或 ndarray 对象传递。 False : 将每一行或每一列作为一个Series传递给函数。True : 传递的函数将接收ndarray对象。如果您只是应用一个NumPy约简函数，这将获得更好的性能。

​	***result_type***：**{‘expand’, ‘reduce’, ‘broadcast’, None}, default None**

​		这些只在axis=1(列)时起作用:

​			‘expand’ : 类似列表的结果将转换为列。

​			‘reduce’ : 如果可能，返回一个Series，而不是展开类似列表的结果。这是‘expand’的反义词。

​			‘broadcast’ : 结果将广播到DataFrame的原始形状，保留原始索引和列。

​		默认行为(None)取决于应用函数的返回值:类似列表的结果将作为这些结果的Series返回。但是，如果apply函数返回一个Series，这些列就会展开为列。

​	***args***：**tuple**

​		除了array/series外，还要传递给func的位置参数。

​	**kwargs：

​		要作为关键字参数传递给func的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.apply.html)

#### **==DataFrame.applymap==**(func, na_action=None, **kwargs)

###### 将函数应用于Dataframe元素。此方法应用一个函数，该函数接受并向DataFrame的每个元素返回一个标量。

##### 参数设置：

​	***func***：**callable**

​		可调用的函数，从一个值返回一个值。

​	***na_action***：{None, ‘ignore’}, default None

​		如果‘ ignore’，则传播 NaN 值，而不将它们传递给 func。

​	***\*kwds**：

​		要作为关键字参数传递给func的其他关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.applymap.html)

#### **==DataFrame.pipe==**(func, *args, **kwargs)

###### 如果需要在链式方法中调用函数，这时候就可以考虑使用 pipe() 方法。它可以返回经过函数处理后的任意类型和形式的数据。

##### 参数设置：

​	***func***：**function**

​		应用于系列/数据帧的函数。args 和 kwargs 被传递到 func。或者是一个（callable，data_keyword）元组，其中 data_keyword 是一个字符串，表示需要Series/DataFrame 的 callable 关键字

​	***args***：**iterable, optional**

​		传入 func 的位置参数。

​	***kwargs***：**mapping, optional**

​		传入 func 的关键字参数字典

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pipe.html)

#### **==DataFrame.agg\aggregate==**(func=None, axis=0, *args, **kwargs)

###### 在指定的轴上使用一个或多个操作进行聚合。别名：aggregate

##### 参数设置：

​	**func** : function, str, list 或 dict

​		函数，用于聚合数据。如果是函数，则必须在传递DataFrame或传递到DataFrame.apply时工作。接受的组合是:

​			function

​			string function name

​			list of functions and/or function names, e.g. [np.sum, 'mean']

​			dict of axis labels -> functions, function names or list of such.

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		如果0或' index ':应用函数到每一列。如果1或‘columns’:应用函数到每一行。

​	***args**：

​		要传递给func的位置参数。

​	**kwargs：

​		要传递给func的关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.agg.html)

#### ==**DataFrame.transform**==(func, axis=0, *args, **kwargs)

###### 调用func自己产生一个改变值的和自己的相同的轴长度的DataFrame

##### 参数设置：

​	***func***：function, str, list-like or dict-like

​		函数，用于聚合数据。如果是函数，则必须在传递DataFrame或传递到DataFrame.apply时工作。接受的组合是:

​			function

​			string function name

​			list of functions and/or function names, e.g. [np.sum, 'mean']

​			dict of axis labels -> functions, function names or list of such.

​	**axis**：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		如果0或' index ':应用函数到每一列。如果1或‘columns’:应用函数到每一行。

​	***args****：

​		要传递给func的位置参数。

​	**kwargs：

​		要传递给func的关键字参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.transform.html)

