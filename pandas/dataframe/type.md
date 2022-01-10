- [==**pandas.DataFrame**==(data=None, index=None, columns=None, dtype=None, copy=None)](#pandasdataframedatanone-indexnone-columnsnone-dtypenone-copynone)
    - [创建数据框](#创建数据框)
  - [参数设置：](#参数设置)
- [官网](#官网)
- [==**DataFrame.dtypes**==](#dataframedtypes)
    - [这将返回一个具有每列数据类型的series。结果的索引是原始 DataFrame 的列。具有混合类型的列与 object dtype 一起存储。See the User Guide for more.](#这将返回一个具有每列数据类型的series结果的索引是原始-dataframe-的列具有混合类型的列与-object-dtype-一起存储see-the-user-guide-for-more)
- [官网](#官网-1)
- [**==DataFrame.astype==**(dtype, copy=True, errors='raise')](#dataframeastypedtype-copytrue-errorsraise)
    - [将pandas对象强制转换为指定的类型](#将pandas对象强制转换为指定的类型)
  - [参数设置：](#参数设置-1)
- [官网](#官网-2)
- [**==DataFrame.convert_dtypes==**(infer_objects=True, convert_string=True, convert_integer=True, convert_boolean=True, convert_floating=True)](#dataframeconvert_dtypesinfer_objectstrue-convert_stringtrue-convert_integertrue-convert_booleantrue-convert_floatingtrue)
    - [使用支持 pd.NA 的 dtypes 将列转换为最佳的 dtype。](#使用支持-pdna-的-dtypes-将列转换为最佳的-dtype)
  - [参数设置：](#参数设置-2)
- [官网](#官网-3)
- [==**DataFrame.infer_objects()**==](#dataframeinfer_objects)
    - [尝试为对象列推断更好的 dtype。尝试对对象类型的列进行软转换，保持非对象列和不可转换列不变。推理规则与正常的 Series/DataFrame 构造期间相同。](#尝试为对象列推断更好的-dtype尝试对对象类型的列进行软转换保持非对象列和不可转换列不变推理规则与正常的-seriesdataframe-构造期间相同)
- [官网](#官网-4)
- [==**DataFrame.sparse.density**==](#dataframesparsedensity)
    - [非稀疏点与总(密集)数据点的比率。](#非稀疏点与总密集数据点的比率)
- [官网](#官网-5)
- [**==DataFrame.sparse.from_spmatrix==(data, *index=None*, *columns=None*)**](#dataframesparsefrom_spmatrixdata-indexnone-columnsnone)
    - [从一个 scipy 稀疏矩阵创建一个新的 DataFrame。](#从一个-scipy-稀疏矩阵创建一个新的-dataframe)
  - [参数设置：](#参数设置-3)
- [官网](#官网-6)
- [==**DataFrame.sparse.**to_coo==()](#dataframesparseto_coo)
    - [返回框架内容作为一个稀疏的 SciPy COO 矩阵。](#返回框架内容作为一个稀疏的-scipy-coo-矩阵)
- [官网](#官网-7)
- [==**DataFrame.sparse.**to_dense==()](#dataframesparseto_dense)
    - [将具有稀疏值的 DataFrame 转换为稠密值。](#将具有稀疏值的-dataframe-转换为稠密值)
- [官网](#官网-8)
- [==**DataFrame.**from_dict==**(**data**,** *orient='columns'***,** *dtype=None***,** *columns=None***)**](#dataframefrom_dictdata-orientcolumns-dtypenone-columnsnone)
    - [从类数组或类数组的 dict 构造数据模型。根据列或允许 dtype 规范的索引从字典创建 datatrame 对象。](#从类数组或类数组的-dict-构造数据模型根据列或允许-dtype-规范的索引从字典创建-datatrame-对象)
  - [参数设置：](#参数设置-4)
- [官网](#官网-9)
- [==**DataFrame.**from_records==**(**data**,** *index=None***,** *exclude=None***,** *columns=None***,** *coerce_float=False***,** *nrows=None***)**](#dataframefrom_recordsdata-indexnone-excludenone-columnsnone-coerce_floatfalse-nrowsnone)
    - [将结构化或记录 ndarray 转换为 DataFrame。从结构化 ndarray、元组或 dicts 序列或 DataFrame 创建一个 DataFrame 对象。](#将结构化或记录-ndarray-转换为-dataframe从结构化-ndarray元组或-dicts-序列或-dataframe-创建一个-dataframe-对象)
  - [参数设置：](#参数设置-5)
- [官网](#官网-10)

#### ==**pandas.DataFrame**==(data=None, index=None, columns=None, dtype=None, copy=None)

###### 创建数据框

##### 参数设置：

​	***data***：**ndarray (structured or homogeneous), Iterable, dict, or DataFrame**

​		Dict 可以包含 Series、 array、 constants、 dataclass 或 list-like 对象。如果数据是 Dict，则列顺序遵循插入顺序。

​	***index***: **Index or array-like**

​		用于生成框架的索引。如果输入数据中没有索引信息，也没有提供索引，则默认为 RangeIndex。

​	***columns***: **Index or array-like**

​		列索引，表头，如果没有指定会自动生成 RangeIndex (0, 1, 2, …, n)

​	***dtype***：**dtype, default None**

​		要强制的数据类型。只允许一个 dtype。如果没有，请推断。

​	***copy***：**bool or None, default None**

​		从输入复制数据。对于 dict 数据，默认值 None 的行为类似于 copy=True。对于 DataFrame 或 2d ndarray 输入，默认值 None 的行为类似于 copy=False

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html#pandas.DataFrame)

#### ==**DataFrame.dtypes**==

###### 这将返回一个具有每列数据类型的series。结果的索引是原始 DataFrame 的列。具有混合类型的列与 object dtype 一起存储。See [the User Guide](https://pandas.pydata.org/docs/user_guide/basics.html#basics-dtypes) for more.

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dtypes.html)

#### **==DataFrame.astype==**(dtype, copy=True, errors='raise')

###### 将pandas对象强制转换为指定的类型

##### 参数设置：

​	***dtype***：**data type, or dict of column name -> data type**

​		使用numpy.dtype或Python类型，将整个pandas对象强制转换为相同的类型。或者，使用{col：dtype，...}，其中col是列标签，dtype是numpy.dtype或Python类型，用于将一个或多个DataFrame列转换为特定于列的类型。

​	***copy***：**bool, default True**

​		返回副本时copy=True（设置copy=False为更改值时要非常小心 ，然后可能会传播到其他pandas对象）。

​	***errors***：**{‘raise’, ‘ignore’}, default ‘raise’**

​		控制提供dtype的无效数据的异常。raise ：允许引发异常；ignore：抑制异常。出错时返回原始对象

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.astype.html)

#### **==DataFrame.convert_dtypes==**(infer_objects=True, convert_string=True, convert_integer=True, convert_boolean=True, convert_floating=True)

###### 使用支持 pd.NA 的 dtypes 将列转换为最佳的 dtype。

##### 参数设置：

​	***infer_objects***：**bool, default True**

​			是否将对象dtypes转换为最佳类型。

​	***convert_string***：**bool, default True**

​		对象dtype是否应转换为StringDtype()。

​	***convert_integer***：**bool, default True**

​		是否(如果可能)转换为整数扩展类型。

​	***convert_boolean***：**bool, default True**

​		对象dtype是否应转换为BooleanDtypes()。

​	***convert_floating***：**bool, default True**

​		如果可能，是否可以转换为浮动扩展类型。如果 convert_integer 也为 True，那么如果浮点数可以忠实地计算为整数，那么将优先选择整数 dtypes。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.convert_dtypes.html)

#### ==**DataFrame.infer_objects()**==

###### 尝试为对象列推断更好的 dtype。尝试对对象类型的列进行软转换，保持非对象列和不可转换列不变。推理规则与正常的 Series/DataFrame 构造期间相同。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.infer_objects.html)

#### ==**DataFrame.sparse.density**==

###### 非稀疏点与总(密集)数据点的比率。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sparse.density.html)

#### **==DataFrame.sparse.from_spmatrix==(data, *index=None*, *columns=None*)**

###### 从一个 scipy 稀疏矩阵创建一个新的 DataFrame。

##### 参数设置：

​	**data：scipy.sparse.spmatrix**

​		必须可转换为 csc 格式。

​	**index, columns：Index, optional**

​		用于生成的 DataFrame 的行和列标签。默认为 RangeIndex。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sparse.from_spmatrix.html)

#### ==**DataFrame.sparse.**to_coo==()

###### 返回框架内容作为一个稀疏的 SciPy COO 矩阵。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sparse.to_coo.html)

#### ==**DataFrame.sparse.**to_dense==()

###### 将具有稀疏值的 DataFrame 转换为稠密值。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sparse.to_dense.html)

#### ==**DataFrame.**from_dict==**(**data**,** *orient='columns'***,** *dtype=None***,** *columns=None***)**

###### 从类数组或类数组的 dict 构造数据模型。根据列或允许 dtype 规范的索引从字典创建 datatrame 对象。

##### 参数设置：

​	***data*：dict**

​		Of the form {field : array-like} or {field : dict}.

​	***orient*：{‘columns’, ‘index’}, default ‘columns’**

​		数据的“方向”。如果传递 dict 的键应该是结果 DataFrame 的列，则传递“ columns”(默认值)。否则，如果键应该是行，则传递“ index”。

​	***dtype*：dtype, default None**

​		要强制执行的数据类型，否则推断。

​	***columns*：list, default None**

​		当 orient = ‘ index’时使用的列标签。如果与 orient = ‘ columns’一起使用，将引发 ValueError。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.from_dict.html)

#### ==**DataFrame.**from_records==**(**data**,** *index=None***,** *exclude=None***,** *columns=None***,** *coerce_float=False***,** *nrows=None***)**

###### 将结构化或记录 ndarray 转换为 DataFrame。从结构化 ndarray、元组或 dicts 序列或 DataFrame 创建一个 DataFrame 对象。

##### 参数设置：

​	***data*：structured ndarray, sequence of tuples or dicts, or DataFrame**

​		结构化输入数据。

​	***index*：str, list of fields, array-like**

​		用作索引的数组字段，或者用作要使用的特定输入标签集。

​	***exclude*：sequence, default None**

​		要排除的列或字段。

​	***columns*：sequence, default None**

​		要使用的列名。如果传递的数据没有与之关联的名称，则此参数提供列的名称。否则，此参数指示结果中列的顺序(在数据中未找到的任何名称都将变为全 na 列)。

​	***coerce_float*：bool, default False**

​		尝试将非字符串、非数值对象(如 Decimal. Decimal)的值转换为浮点数，这对 SQL 结果集很有用。

​	***nrows*：int, default None**

​		如果数据是迭代器，则要读取的行数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.from_records.html)



