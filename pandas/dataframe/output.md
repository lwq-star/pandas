#### ==**DataFrame.**to_parquet==**(**path=None**,** *engine='auto'***,** *compression='snappy'***,** *index=None***,** *partition_cols=None***,** *storage_options=None***,** ***kwargs***)

###### 将DataFrame写入二进制镶木包格式。此函数将DataFrame写为 [parquet file](https://parquet.apache.org/).。您可以选择不同的木质后端，并具有压缩选项。有关详细信息，请参阅“ [the user guide](https://pandas.pydata.org/docs/user_guide/io.html#io-parquet) ”。

##### 参数设置：

​	***path***：**str or file-like object, default None**

​		如果是字符串，则在编写分区数据集时，它将用作根目录路径。通过类似文件的对象，我们使用 write ()方法引用对象，比如文件句柄(例如通过内建的 open 函数)或 io。BytesIO.引擎快拼花不接受类似文件的对象。如果 path 为 None，则返回一个字节对象。

​	***engine***：**{‘auto’, ‘pyarrow’, ‘fastparquet’}, default ‘auto’**

​		使用拼花图书馆。如果是‘ auto’，则使用 io.parquet.engine 选项。引擎的默认行为是尝试“ pyarrow”，如果“ pyarrow”不可用，则退回到“ fastparquet”。

​	***compression***：**{‘snappy’, ‘gzip’, ‘brotli’, None}, default ‘snappy’**

​		要使用的压缩名称。不使用压缩时使用 None。

​	***index***：**bool, default None**

​		如果为 True，则在文件输出中包含数据流的索引(es)。如果为 False，则不会将它们写入文件。如果没有，类似于 True，数据流的索引将被保存。但是，RangeIndex 不是保存为值，而是作为元数据的一个范围存储，因此它不需要太多空间，而且速度更快。其他索引将作为列包含在文件输出中。

​	***partition_cols***：**list, optional, default None**

​		用于对数据集进行分区的列名。列按照给定的顺序进行分区。如果 path 不是字符串，则必须为 None。

​	***storage_options***：**dict, optional**

​		对特定存储连接有意义的额外选项，例如主机、端口、用户名、密码等。对于 HTTP (s) url，键值对作为头选项被转发到 urllib。对于其他 url (例如以“ s3://”和“ gcs://”开头) ，键值对被转发到 fsspec。详细信息请参阅 fsspec 和 urllib。

​	***\*kwargs**：传递到实木复合地板库的其他参数。有关详细信息，请参阅 pandas io。

##### 注意：

​	这个函数需要 [fastparquet](https://pypi.org/project/fastparquet) or [pyarrow](https://arrow.apache.org/docs/python/) library.

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_parquet.html)

#### ==**DataFrame.**to_pickle==**(**path**,** *compression='infer'***,** *protocol=5***,** *storage_options=None***)**

###### 对象到文件的酸洗(序列化)。

##### 参数设置：

​	***path*：str**

​		存储 pickle 对象的文件路径。

​	***compression*：{‘infer’, ‘gzip’, ‘bz2’, ‘zip’, ‘xz’, None}, default ‘infer’**

​		表示要在输出文件中使用的压缩的字符串。默认情况下，从指定路径的文件扩展名推断。压缩模式可能是以下任何一个可能的值: {‘ infer’，‘ gzip’，‘ bz2’，‘ zip’，‘ xz’，‘ None }。如果压缩模式是‘ infer’，而 path _ 或 _ buf 是类似于路径的，那么从以下扩展中检测压缩模式:。“ gz”，“。Bz2.“压缩”或“。我不知道你在说什么 i don’t know what you’re talking。(否则没有压缩)。如果 dict 给出和模式是“ zip”或推断为“ zip”，其他条目作为附加压缩选项传递。

​	***protocol*：int**

​		Int 表示 pickler 应该使用哪个协议，默认为 HIGHEST _ protocol (参见[1]第12.1.2段)。可能的值是0,1,2,3,4,5。协议参数的负值等效于将其值设置为 HIGHEST _ protocol。[参考](https://docs.python.org/3/library/pickle.html)

​	***storage_options*：dict, optional****

​		对特定存储连接有意义的额外选项，例如主机、端口、用户名、密码等。对于 HTTP (s) url，键值对作为头选项被转发到 urllib。对于其他 url (例如以“ s3://”和“ gcs://”开头) ，键值对被转发到 fsspec。详细信息请参阅 fsspec 和 urllib。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_pickle.html)

#### ==**DataFrame.**to_csv==**(**path_or_buf=None**,** *sep=','***,** *na_rep=''***,** *float_format=None***,** *columns=None***,** *header=True***,** *index=True***,** *index_label=None***,** *mode='w'***,** *encoding=None***,** *compression='infer'***,** *quoting=None***,** *quotechar='"'***,** *line_terminator=None***,** *chunksize=None***,** *date_format=None***,** *doublequote=True***,** *escapechar=None***,** *decimal='.'***,** *errors='strict'***,** *storage_options=None***)**

###### 将对象写入逗号分隔值文件(csv)。

##### 参数设置：

​	***path_or_buf***：**str or file handle, default None**

​		文件路径或对象，如果没有提供，结果将作为字符串返回。如果传递了非二进制文件对象，则应该用换行符 =”打开它，禁用通用换行符。如果传递了一个二进制文件对象，则 mode 可能需要包含一个“ b”。

​	***sep***：**str, default ‘,’**

​		输出文件的字符串长度为1. 字段分隔符。

​	***na_rep***：**str, default ‘’**

​		缺失的数据表示，默认是空

​	***float_format***：**str, default None**

​		浮点数的格式化字符串

​	***columns***：**sequence, optional**

​		输出的列

​	***header***：**bool or list of str, default True**

​		写出列的名称，如果给出了字符串列表，则假定它是列名的别名

​	***index_label***：**str or sequence, or False, default None**

​		如果需要，可以使用索引列的列标签。如果没有给出，且标题和索引为True，则使用索引名称。如果数据文件使用多索引，则应该使用这个序列。如果值为False，不打印索引字段。在R中使用index_label=False 更容易导入索引。

​	***mode***：**str**

​		Python写入模式，默认为“w”

​	***encoding***：**str, optional**

​		表示在输出文件中使用的编码的字符串，默认为“ utf-8”。如果 path _ 或 _buf 是非二进制文件对象，则不支持编码。

​	***compression***：**str or dict, default ‘infer’**

​		如果为 str，则表示压缩模式。如果 dict，“方法”的值是压缩模式。压缩模式可能是以下任何一个可能的值: {‘ infer’，‘ gzip’，‘ bz2’，‘ zip’，‘ xz’，‘ None }。如果压缩模式是‘ infer’，而 path _ 或 _ buf 是类似于路径的，那么从以下扩展中检测压缩模式:。“ gz”，“。Bz2.“压缩”或“。我不知道你在说什么 i don’t know what you’re talking。(否则没有压缩)。如果 dict given 和 mode 是{‘ zip’、‘ gzip’、‘ bz2’}中的一个，或者推断为上面的一个，其他条目作为附加压缩选项传递。

​	***line_terminator***：**str, optional**

​		在输出文件中使用的换行字符或字符序列

​	***quoting***：**optional constant from csv module**

​		默认值为to_csv.QUOTE_MINIMAL。如果设置了浮点格式，那么浮点将转换为字符串，因此csv.QUOTE_NONNUMERIC会将它们视为非数值的。

​	***chunksize***：**int or None**

​		一次输出指定行数

​	***date_format***：**str, default None**

​		字符串对象转换为日期时间对象

​	***escapechar***：**str, default None**

​		长度为1的字符串。适当时用于转义 sep 和 quotechar

​	***decimal***：**str, default ‘.’**

​		字符识别为小数点分隔符。例如：欧洲数据使用 ’，’

​	***errors***：**str, default ‘strict’**

​		指定如何处理编码和解码错误。有关完整的选项列表，请参见 [`open()`](https://docs.python.org/3/library/functions.html#open) 的错误参数。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_csv.html)

#### ==**DataFrame.**to_hdf==**(**path_or_buf**,** *key***,** *mode='a'***,** *complevel=None***,** *complib=None***,** *append=False***,** *format=None***,** *index=True***,** *min_itemsize=None***,** *nan_rep=None***,** *dropna=None***,** *data_columns=None***,** *errors='strict'***,** *encoding='UTF-8'***)**

###### 使用 HDFStore 将包含的数据写入 hdf5文件。HDF 是自我描述的，允许应用程序在没有外部信息的情况下解释文件的结构和内容。一个 HDF 文件可以保存多个相关对象，可以作为一个组或单个对象访问这些对象。为了向现有的 HDF 文件中添加另一个 datatrame 或 Series，请使用 append 模式和另一个键。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_hdf.html)

#### ==**DataFrame.**to_sql==**(**name**,** *con***,** *schema=None***,** *if_exists='fail'***,** *index=True***,** *index_label=None***,** *chunksize=None***,** *dtype=None***,** *method=None***)**

###### 将存储在 DataFrame 中的记录写入 SQL 数据库。支持 SQLAlchemy [1]支持的数据库。可以新创建、追加或覆盖表。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_sql.html)

#### **DataFrame.**to_dict**(**orient='dict'**,** *into=<class 'dict'>***)**

###### 将 DataFrame 转换为字典。键值对的类型可以使用参数进行自定义(参见下面)。

##### 参数设置：

​	**orient：str {‘dict’, ‘list’, ‘series’, ‘split’, ‘records’, ‘index’}**

​		确定字典值的类型。

​			‘dict’ (default) : dict like {column -> {index -> value}}

​			‘list’ : dict like {column -> [values]}

​			‘series’ : dict like {column -> Series(values)}

​			‘split’ : dict like {‘index’ -> [index], ‘columns’ -> [columns], ‘data’ -> [values]}

​			‘records’ : list like [{column -> value}, … , {column -> value}]

​			‘index’ : dict like {index -> {column -> value}}

​		缩写是允许的。 s 表示系列和 sp 表示分裂。

​	**into：class, default dict**

​		collections.abc.mapped子类用于返回值中的所有映射。可以是实际类或所需映射类型的空实例。如果您想要集合.Defaultdict，您必须通过它初始化。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_dict.html)

#### ==**DataFrame.**to_excel==**(**excel_writer**,** *sheet_name='Sheet1'***,** *na_rep=''***,** *float_format=None***,** *columns=None***,** *header=True***,** *index=True***,** *index_label=None***,** *startrow=0***,** *startcol=0***,** *engine=None***,** *merge_cells=True***,** *encoding=None***,** *inf_rep='inf'***,** *verbose=True***,** *freeze_panes=None***,** *storage_options=None***)**

###### 将对象写入 Excel 工作表。将单个对象写入 Excel。Xlsx 文件只需要指定一个目标文件名。要写入多个工作表，必须创建一个带有目标文件名的 ExcelWriter 对象，并在文件中指定要写入的工作表。可以通过指定唯一的工作表 _ 名称来写入多个工作表。将所有数据写入文件后，必须保存更改。请注意，使用已经存在的文件名创建一个 ExcelWriter 对象将导致现有文件的内容被擦除。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_excel.html)

#### ==**DataFrame.**to_json==**(**path_or_buf=None**,** *orient=None***,** *date_format=None***,** *double_precision=10***,** *force_ascii=True***,** *date_unit='ms'***,** *default_handler=None***,** *lines=False***,** *compression='infer'***,** *index=True***,** *indent=None***,** *storage_options=None***)**

###### 将对象转换为 JSON 字符串。注意，NaN 和 None 将转换为 null，而 datetime 对象将转换为 UNIX 时间戳。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_json.html)

#### ==**DataFrame.**to_html==**(**buf=None**,** *columns=None***,** *col_space=None***,** *header=True***,** *index=True***,** *na_rep='NaN'***,** *formatters=None***,** *float_format=None***,** *sparsify=None***,** *index_names=True***,** *justify=None***,** *max_rows=None***,** *max_cols=None***,** *show_dimensions=False***,** *decimal='.'***,** *bold_rows=True***,** *classes=None***,** *escape=True***,** *notebook=False***,** *border=None***,** *table_id=None***,** *render_links=False***,** *encoding=None***)**

###### 将 DataFrame 呈现为 HTML 表。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_html.html)

#### ==**DataFrame.**to_feather==**(**path**,** ***kwargs***)

###### 编写一个二进制 Feather 格式的 DataFrame。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_feather.html)

#### ==**DataFrame.**to_latex==**(**buf=None**,** *columns=None***,** *col_space=None***,** *header=True***,** *index=True***,** *na_rep='NaN'***,** *formatters=None***,** *float_format=None***,** *sparsify=None***,** *index_names=True***,** *bold_rows=False***,** *column_format=None***,** *longtable=None***,** *escape=None***,** *encoding=None***,** *decimal='.'***,** *multicolumn=None***,** *multicolumn_format=None***,** *multirow=None***,** *caption=None***,** *label=None***,** *position=None***)**

###### 将对象呈现为 LaTeX 表、长表或嵌套表/表格。需要 usepackage { booktabs }。输出可以复制/粘贴到主 LaTeX 文档中，也可以使用输入{ table.tex }从外部文件中读取。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_latex.html)

#### ==**DataFrame.**to_stata==**(**path**,** *convert_dates=None***,** *write_index=True***,** *byteorder=None***,** *time_stamp=None***,** *data_label=None***,** *variable_labels=None***,** *version=114***,** *convert_strl=None***,** *compression='infer'***,** *storage_options=None***)**

###### 将 DataFrame 对象导出为 statadta 格式。将 DataFrame 写入 Stata 数据集文件。“ dta”文件包含 Stata 数据集。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_stata.html)

#### ==**DataFrame.**to_gbq==**(**destination_table**,** *project_id=None***,** *chunksize=None***,** *reauth=False***,** *if_exists='fail'***,** *auth_local_webserver=False***,** *table_schema=None***,** *location=None***,** *progress_bar=True***,** *credentials=None***)**

###### 编写一个 DataFrame 到一个 Google BigQuery 表。这个函数需要 pandas-gbq 包。有关身份验证指南，请参阅 [How to authenticate with Google BigQuery](https://pandas-gbq.readthedocs.io/en/latest/howto/authentication.html) 进行身份验证指南。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_gbq.html)

#### ==**DataFrame.**to_records==**(**index=True**,** *column_dtypes=None***,** *index_dtypes=None***)**

###### 将dataframe转换为numpy记录阵列。如果请求，索引将被包含为记录数组的第一个字段。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_records.html)

#### ==**DataFrame.**to_string==**(**buf=None**,** *columns=None***,** *col_space=None***,** *header=True***,** *index=True***,** *na_rep='NaN'***,** *formatters=None***,** *float_format=None***,** *sparsify=None***,** *index_names=True***,** *justify=None***,** *max_rows=None***,** *min_rows=None***,** *max_cols=None***,** *show_dimensions=False***,** *decimal='.'***,** *line_width=None***,** *max_colwidth=None***,** *encoding=None***)**

###### 将 DataFrame 呈现为控制台友好的表格输出。

##### 参数设置：

​	***buf*：str, Path or StringIO-like, optional, default None**

​		要写入的缓冲区。如果没有，则输出作为字符串返回。

​	***columns*：sequence, optional, default None**

​		要写入的列的子集。默认情况下写入所有列。

​	***col_space*：int, list or dict of int, optional**

​		每列的最小宽度。

​	***header*：bool or sequence, optional**

​		写出列的名称。如果给出了字符串列表，则假定它是列名的别名

​	***index*：bool, optional, default True**

​		是否打印索引(行)标签。

​	***na_rep*：str, optional, default ‘NaN’**

​		要使用的 NaN 的字符串表示形式。

​	***formatters*：list, tuple or dict of one-param. functions, optional**

​		根据位置或名称应用于列元素的格式化程序函数。每个函数的结果必须是一个 unicode 字符串。List/tuple 的长度必须等于列数。

​	***float_format*：one-parameter function, optional, default None**

​		格式化程序函数应用于列的元素(如果它们是浮动的)。这个函数必须返回一个 unicode 字符串，并且只应用于非 NaN 元素，而 NaN 由 na _ rep 处理。

​	***sparsify*：bool, optional, default True**

​		将 DataFrame 设置为 False，并使用分层索引在每行打印每个多索引键。

​	***index_names*：bool, optional, default True**

​		打印索引的名称。

​	***justify*：str, default None**

​		如何调整列标签。如果 None 使用打印配置中的选项(由 set_option 控制) ，“右”开箱即用。有效值为

​			left，right，center，justify，justify-all，start，end，inherit，match-parent，initial，unset.

​	***max_rows*：int, optional**

​		在控制台中显示的最大行数。

​	***min_rows*：int, optional**

​		要在控制台中显示的被截断的响应行的行数(当行数高于 max_rows 时)。

​	***max_cols*：int, optional**

​		在控制台中显示的最大列数。

​	***show_dimensions*：bool, default False**

​		显示 DataFrame 维度(按列数显示的行数)。

​	***decimal*：str, default ‘.’**

​		在欧洲被认为是小数点的字符，例如‘ ,’。

​	***line_width*：int, optional**

​		宽度以字符换行。

​	***max_colwidth*：int, optional**

​		最大宽度截断每列个字符。默认情况下，没有限制。

​	***encoding*：str, default “utf-8”**

​		设置字符编码。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_string.html)

#### ==**DataFrame.**to_clipboard==**(**excel=True**,** *sep=None***,** ***kwargs***)

###### 将对象复制到系统剪贴板。将对象的文本表示写入系统剪贴板。例如，这可以粘贴到 Excel 中。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_clipboard.html)

#### ==**DataFrame.**to_markdown==**(**buf=None**,** *mode='wt'***,** *index=True***,** *storage_options=None***,** ***kwargs***)

###### 在Markdown友好格式中打印DataFrame。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_markdown.html)

