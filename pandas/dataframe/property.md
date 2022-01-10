- [**==DataFrame.info==**(verbose=None, buf=None, max_cols=None, memory_usage=None, show_counts=None, null_counts=None)](#dataframeinfoverbosenone-bufnone-max_colsnone-memory_usagenone-show_countsnone-null_countsnone)
    - [此方法打印有关 DataFrame 的信息，包括索引类型和列、非空值和内存使用情况。](#此方法打印有关-dataframe-的信息包括索引类型和列非空值和内存使用情况)
  - [参数设置：](#参数设置)
- [官网 [中文参考](https://www.cjavapy.com/article/535/)](#官网-中文参考)
- [==**DataFrame.ndim**==](#dataframendim)
    - [返回一个 int，表示轴/数组维数。如果是 Series，返回1，如果是 DataFrame，则返回2。](#返回一个-int表示轴数组维数如果是-series返回1如果是-dataframe则返回2)
- [官网](#官网)
- [==**DataFrame.size**==](#dataframesize)
    - [返回一个 int，表示此对象中的元素数。如果是 Series，则返回行数。如果是 DataFrame，则返回行数乘以列数。](#返回一个-int表示此对象中的元素数如果是-series则返回行数如果是-dataframe则返回行数乘以列数)
- [官网](#官网-1)
- [==**DataFrame.shape**==](#dataframeshape)
    - [返回一个表示 DataFrame 维度的元组](#返回一个表示-dataframe-维度的元组)
- [官网](#官网-2)
- [**==DataFrame.memory_usage==**(index=True, deep=False)](#dataframememory_usageindextrue-deepfalse)
    - [以字节为单位返回每列的内存使用情况。内存使用可以选择性地包括索引和对象 dtype 元素的贡献。这个值默认显示在 DataFrame.info 中，可以通过将 pandas.options.display.memory _ usage 设置为 False 来抑制。](#以字节为单位返回每列的内存使用情况内存使用可以选择性地包括索引和对象-dtype-元素的贡献这个值默认显示在-dataframeinfo-中可以通过将-pandasoptionsdisplaymemory-_-usage-设置为-false-来抑制)
  - [参数设置：](#参数设置-1)
- [官网](#官网-3)
- [**==DataFrame.set_flags==**(*, copy=False, allows_duplicate_labels=None)](#dataframeset_flags-copyfalse-allows_duplicate_labelsnone)
    - [返回一个带有更新标志的新对象](#返回一个带有更新标志的新对象)
  - [参数设置：](#参数设置-2)
- [官网](#官网-4)
- [**==pandas.Flags==**(obj, *, allows_duplicate_labels)](#pandasflagsobj--allows_duplicate_labels)
    - [适用于Pandas对象的标志。](#适用于pandas对象的标志)
  - [参数设置：](#参数设置-3)
- [官网](#官网-5)
- [==DataFrame.attrs==](#dataframeattrs)
    - [此数据集的全局属性字典。](#此数据集的全局属性字典)
- [官网](#官网-6)
- [==**DataFrame.**style==](#dataframestyle)
    - [返回一个 Styler 对象。包含用于构建 DataFrame 的样式化 HTML 表示的方法。](#返回一个-styler-对象包含用于构建-dataframe-的样式化-html-表示的方法)

#### **==DataFrame.info==**(verbose=None, buf=None, max_cols=None, memory_usage=None, show_counts=None, null_counts=None)

###### 此方法打印有关 DataFrame 的信息，包括索引类型和列、非空值和内存使用情况。

##### 参数设置：

​	***data*：DataFrame**

​	***verbose***：**bool, optional**

​		是否打印完整的摘要。默认情况下，遵循pandas.options.display.max_info_columns中的设置 。

​	***buf***：**writable buffer, defaults to sys.stdout**

​		将输出发送到哪里。默认情况下，输出将打印到sys.stdout。如果需要进一步处理输出，请传递可写缓冲区。

​	***max_cols***：**int, optional**

​		何时从详细输出切换到截断输出。如果DataFrame的列数超过max_cols列，则使用截断的输出。默认情况下，使用中的设置 pandas.options.display.max_info_columns。

​	***memory_usage***：**bool, str, optional**

​		指定是否应显示DataFrame元素（包括索引）的总内存使用情况。默认情况下，这遵循pandas.options.display.memory_usage设置

​	***show_counts***：**bool, optional**

​		是否显示非空计数。默认情况下，只有当DataFrame小于Pandas.Options.display.max_info_rows和pandas.options.display.max_info_columns时，才会显示此内容。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.info.html) [中文参考](https://www.cjavapy.com/article/535/)

#### ==**DataFrame.ndim**==

###### 返回一个 int，表示轴/数组维数。如果是 Series，返回1，如果是 DataFrame，则返回2。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.ndim.html)

#### ==**DataFrame.size**==

###### 返回一个 int，表示此对象中的元素数。如果是 Series，则返回行数。如果是 DataFrame，则返回行数乘以列数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.size.html)

#### ==**DataFrame.shape**==

###### 返回一个表示 DataFrame 维度的元组

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.shape.html)

#### **==DataFrame.memory_usage==**(index=True, deep=False)

###### 以字节为单位返回每列的内存使用情况。内存使用可以选择性地包括索引和对象 dtype 元素的贡献。这个值默认显示在 DataFrame.info 中，可以通过将 pandas.options.display.memory _ usage 设置为 False 来抑制。

##### 参数设置：

​	***index*** ：**bool, default True**

​		指定是否在返回的Series中包括DataFrame索引的内存使用情况。如果index=True索引的内存使用率在输出中的第一项。

​	***deep*** ：**bool, default False**

​		如果为True，则通过询问对象类型来深入了解数据的系统级内存消耗，并将其包含在返回值中。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.memory_usage.html)

#### **==DataFrame.set_flags==**(*, copy=False, allows_duplicate_labels=None)

###### 返回一个带有更新标志的新对象

##### 参数设置：

​	***allows_duplicate_labels***：**bool, optional**

​		返回的对象是否允许重复标签。

注意：

​	此方法返回一个新对象，该对象是与输入相同的数据的视图。输入或输出值的变化将反映在另一个中。此方法往往用于方法链。“标志”与“元数据”不同。旗帜反映pandas对象的属性(Series 或 DataFrame)。元数据引用数据集的属性，应该存储在 DataFrame.attrs 中。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.set_flags.html)

#### **==pandas.Flags==**(obj, *, allows_duplicate_labels)

###### 适用于Pandas对象的标志。

##### 参数设置：

​	**obj**：**Series or DataFrame**

​		这些标志与之关联的对象。

​	**allows_duplicate_labels**：**bool, default True**

​		是否允许在此对象中使用重复标签。默认情况下，允许重复标签。将其设置为 False 将导致错误。当索引(或 DataFrame 的列)不唯一时引发 DuplicateLabelError，或者任何对重复项的后续操作。更多信息请参见禁止重复标签。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.Flags.html)

#### ==DataFrame.attrs==

###### 此数据集的全局属性字典。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.attrs.html)

#### ==**DataFrame.**style==

###### 返回一个 Styler 对象。包含用于构建 DataFrame 的样式化 HTML 表示的方法。

