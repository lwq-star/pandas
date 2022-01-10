- [==**DataFrame.at_time**==(time, asof=False, axis=None)](#dataframeat_timetime-asoffalse-axisnone)
    - [在特定时间选择值（例如，上午9:30）。](#在特定时间选择值例如上午930)
  - [参数设置：](#参数设置)
- [官网](#官网)
- [**==DataFrame.between_time==**(start_time, end_time, include_start=True, include_end=True, axis=None)](#dataframebetween_timestart_time-end_time-include_starttrue-include_endtrue-axisnone)
    - [选择一天中特定时间之间的值（例如，上午9：00-9：30）。通过设置start_time为晚于end_time，您可以获得不在两次之间的时间。](#选择一天中特定时间之间的值例如上午900-930通过设置start_time为晚于end_time您可以获得不在两次之间的时间)
  - [参数设置：](#参数设置-1)
- [官网](#官网-1)
- [**==DataFrame.first\last==**(offset)](#dataframefirstlastoffset)
    - [一种基于日期偏移量来设置时间序列数据的初始时段\最终时段。在具有日期的DataFrame作为索引时，此函数可以根据日期偏移选择前几行\最后几行。](#一种基于日期偏移量来设置时间序列数据的初始时段最终时段在具有日期的dataframe作为索引时此函数可以根据日期偏移选择前几行最后几行)
  - [参数设置：](#参数设置-2)
- [官网](#官网-2)
- [**==DataFrame.asfreq==**(freq, method=None, how=None, normalize=False, fill_value=None)](#dataframeasfreqfreq-methodnone-hownone-normalizefalse-fill_valuenone)
    - [将TimeSeries转换为指定的频率。可选择提供填充方法来填充/回填缺失值。返回符合指定频率的新索引的原始数据。resample如果需要一个操作（如摘要）来表示新频率的数据，则更合适。](#将timeseries转换为指定的频率可选择提供填充方法来填充回填缺失值返回符合指定频率的新索引的原始数据resample如果需要一个操作如摘要来表示新频率的数据则更合适)
  - [参数设置：](#参数设置-3)
  - [注意：](#注意)
- [官网](#官网-3)
- [==**DataFrame.asof**==(where, subset=None)](#dataframeasofwhere-subsetnone)
    - [返回前最后一行（S）没有任何NaN的地方。不带任何NaN的最后一行（对于where，if list中的每个元素）。在a的情况下，DataFrame没有NaN的最后一行仅考虑列的子集（如果不是None）](#返回前最后一行s没有任何nan的地方不带任何nan的最后一行对于whereif-list中的每个元素在a的情况下dataframe没有nan的最后一行仅考虑列的子集如果不是none)
  - [参数设置：](#参数设置-4)
- [官网](#官网-4)
- [**==DataFrame.shift==**(periods=1, freq=None, axis=0, fill_value=NoDefault.no_default)](#dataframeshiftperiods1-freqnone-axis0-fill_valuenodefaultno_default)
    - [用一个可选的时间频率按所需的周期数移动索引。当频率未通过时，在不重新排列数据的情况下移动索引。如果频率通过(在这种情况下,指数一定日期或日期时间,或将提高NotImplementedError),该指数将会增加使用时间和freq.频率时可以推断出指定为“infer”只要频率或inferred_freq属性设置在索引中。](#用一个可选的时间频率按所需的周期数移动索引当频率未通过时在不重新排列数据的情况下移动索引如果频率通过在这种情况下指数一定日期或日期时间或将提高notimplementederror该指数将会增加使用时间和freq频率时可以推断出指定为infer只要频率或inferred_freq属性设置在索引中)
  - [参数设置：](#参数设置-5)
- [官网](#官网-5)
- [**==DataFrame.resample==**(rule, axis=0, closed=None, label=None, convention='start', kind=None, loffset=None, base=None, on=None, level=None, origin='start_day', offset=None)](#dataframeresamplerule-axis0-closednone-labelnone-conventionstart-kindnone-loffsetnone-basenone-onnone-levelnone-originstart_day-offsetnone)
    - [重新采样time-series数据。频率转换和time series重采样的便捷方法。对象必须具有类似datetime的索引(DatetimeIndex， PeriodIndex或TimedeltaIndex)，或将类似datetime的值传递给on或level关键字。](#重新采样time-series数据频率转换和time-series重采样的便捷方法对象必须具有类似datetime的索引datetimeindex-periodindex或timedeltaindex或将类似datetime的值传递给on或level关键字)
  - [参数设置：](#参数设置-6)
  - [注意：](#注意-1)
- [官网](#官网-6)
- [**==DataFrame.to_period==**(freq=None, axis=0, copy=True)](#dataframeto_periodfreqnone-axis0-copytrue)
    - [将 DataFrame 从 DatetimeIndex 转换为 PeriodIndex。用期望的频率将 DataFrame 从 DatetimeIndex 转换为 PeriodIndex (如果没有通过，则从索引中推断)。](#将-dataframe-从-datetimeindex-转换为-periodindex用期望的频率将-dataframe-从-datetimeindex-转换为-periodindex-如果没有通过则从索引中推断)
  - [参数设置：](#参数设置-7)
- [官网](#官网-7)
- [**==DataFrame.to_timestamp==**(freq=None, how='start', axis=0, copy=True)](#dataframeto_timestampfreqnone-howstart-axis0-copytrue)
    - [期初时间戳的 DatetimeIndex 的强制转换。](#期初时间戳的-datetimeindex-的强制转换)
  - [参数设置：](#参数设置-8)
- [官网](#官网-8)
- [**==DataFrame.tz_convert==**(tz, axis=0, level=None, copy=True)](#dataframetz_converttz-axis0-levelnone-copytrue)
    - [将 tz 感知轴转换为目标时区。](#将-tz-感知轴转换为目标时区)
  - [参数设置：](#参数设置-9)
- [官网](#官网-9)
- [**==DataFrame.tz_localize==**(tz, axis=0, level=None, copy=True, ambiguous='raise', nonexistent='raise')](#dataframetz_localizetz-axis0-levelnone-copytrue-ambiguousraise-nonexistentraise)
    - [将 Series 或 DataFrame 的 tz-naive 索引本地化为目标时区。此操作将索引本地化Series.dt.tz_localize().](#将-series-或-dataframe-的-tz-naive-索引本地化为目标时区此操作将索引本地化seriesdttz_localize)
  - [参数设置：](#参数设置-10)
- [官网](#官网-10)

#### ==**DataFrame.at_time**==(time, asof=False, axis=None)

###### 在特定时间选择值（例如，上午9:30）。

##### 参数设置：

​	***time***： **datetime.time or str**

​	***axis***： **{0 or ‘index’, 1 or ‘columns’}, default 0**

TypeError：如果索引不是DateTimeIndex

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.at_time.html)

#### **==DataFrame.between_time==**(start_time, end_time, include_start=True, include_end=True, axis=None)

###### 选择一天中特定时间之间的值（例如，上午9：00-9：30）。通过设置start_time为晚于end_time，您可以获得不在两次之间的时间。

##### 参数设置：

​	***start_time***： **datetime.time or str**

​		初始时间作为时间过滤器限制。

​	***end_time*** ： **datetime.time or str**

​		结束时间作为时间过滤器限制。

​	***include_start*** ： **bool, default True**

​		开始时间是否需要包括在结果中。

​	***include_end*** ： **bool, default True**

​		结束时间是否需要包括在结果中。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		确定索引或列值的范围时间。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.between_time.html)

#### **==DataFrame.first\last==**(offset)

###### 一种基于日期偏移量来设置时间序列数据的初始时段\最终时段。在具有日期的DataFrame作为索引时，此函数可以根据日期偏移选择前几行\最后几行。

##### 参数设置：

​	***offset*** ：string，DateOffset，dateutil.relativedelta。

​		要选择的数据的偏移长度。例如，“1M”将显示第一个\最后一个月内索引的所有行，“3D”将显示从开始\结束时间计算的包含在前\后三天以内的数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.first.html)

#### **==DataFrame.asfreq==**(freq, method=None, how=None, normalize=False, fill_value=None)

###### 将TimeSeries转换为指定的频率。可选择提供填充方法来填充/回填缺失值。返回符合指定频率的新索引的原始数据。resample如果需要一个操作（如摘要）来表示新频率的数据，则更合适。

##### 参数设置：

​	***freq***： **DateOffset or str**

​		DateOffset对象或字符串

​	***method***： **{‘backfill’/’bfill’, ‘pad’/’ffill’}, default None**

​		用于填充重建索引Series中的孔的方法（请注意，这不会填充已存在的NaN）：

​			'pad'/'ffill'：将最后一次有效结果传播到下一个有效

​			'backfill'/'bfill'：使用NEXT有效结果来填充

​	***how***：**{‘start’, ‘end’}, default end**

​		仅适用于PeriodIndex，请参阅PeriodIndex.asfreq

​	***normalize***： **bool, default False**

​		是否将输出索引重置为午夜

​	***fill_value***：**scalar, optional**

​		用于缺失值的值，在上采样期间应用（请注意，这不会填充已存在的NaN）。

##### 注意：

​	要了解更多关于频率字符串的信息，请参见 [this link](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#offset-aliases).

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.asfreq.html)

#### ==**DataFrame.asof**==(where, subset=None)

###### 返回前最后一行（S）没有任何NaN的地方。不带任何NaN的最后一行（对于where，if list中的每个元素）。在a的情况下，[DataFrame](http://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html#pandas.DataFrame)没有NaN的最后一行仅考虑列的子集（如果不是None）

##### 参数设置：

​	***where***：**date or array-like of dates**

​		返回最后一行之前的日期。

​	***subset***：**str or array-like of str, default** None

​		对于DataFrame，如果不是None，则仅使用这些列来检查NaN。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.asof.html)

#### **==DataFrame.shift==**(periods=1, freq=None, axis=0, fill_value=NoDefault.no_default)

###### 用一个可选的时间频率按所需的周期数移动索引。当频率未通过时，在不重新排列数据的情况下移动索引。如果频率通过(在这种情况下,指数一定日期或日期时间,或将提高NotImplementedError),该指数将会增加使用时间和freq.频率时可以推断出指定为“infer”只要频率或inferred_freq属性设置在索引中。

##### 参数设置：

​	***periods***：**int**

​		要转换的周期数。可以是正数或负数。

​	***freq***：**DateOffset, tseries.offsets, timedelta, or str, optional**

​		从tseries模块或时间规则使用的偏移量（例如 ‘EOM’）。如果指定了freq，则索引值会移位，但数据不会重新对齐。也就是说，如果您想在移位时扩展索引并保留原始数据，请使用freq。如果将freq指定为“infer”，则将从索引的freq或inferred_freq属性推断出来。如果这些属性都不存在，则会引发ValueError

​	***axis***：**{0 or ‘index’, 1 or ‘columns’, None}, default None**

​		转变(Shift)方向。

​	***fill_value***：**object, optional**

​		用于新引入的缺失值的标量值。默认值取决于self的dtype 。对于数字数据，np.nan使用。对于日期时间，时间增量或期间数据等NaT。对于扩展dtype，self.dtype.na_value使用。默认值取决于self的dtype 。对于数字数据，np.nan使用。对于日期时间，时间增量或期间数据等NaT。对于扩展dtype，self.dtype.na_value使用。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.shift.html)

#### **==DataFrame.resample==**(rule, axis=0, closed=None, label=None, convention='start', kind=None, loffset=None, base=None, on=None, level=None, origin='start_day', offset=None)

###### 重新采样time-series数据。频率转换和time series重采样的便捷方法。对象必须具有类似datetime的索引(DatetimeIndex， PeriodIndex或TimedeltaIndex)，或将类似datetime的值传递给on或level关键字。

##### 参数设置：

​	***rule***: **DateOffset, Timedelta or str**

​		表示目标转换的偏移字符串或对象。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		向上采样或向下采样使用哪一个轴。对于级数，默认值为0，即沿着行。必须是DatetimeIndex, TimedeltaIndex或PeriodIndex。

​	***closed***: **{‘right’, ‘left’}, default None**

​		bin区间的哪一边是关闭的。除了‘M’、‘A’、‘Q’、‘BM’、‘BA’、‘BQ’和‘W’之外，所有频率偏移的默认值都是‘left’，它们的默认值都是‘right’。

​	***label***: **{‘right’, ‘left’}, default None**

​		用哪边标签来标记bucket。除了‘M’、‘A’、‘Q’、‘BM’、‘BA’、‘BQ’和‘W’之外，所有频率偏移的默认值都是‘left’，它们的默认值都是‘right’。

​	***convention***: **{‘start’, ‘end’, ‘s’, ‘e’}, default ‘start’**

​		仅对于PeriodIndex，控制是使用规则的开始还是结束。

​	***kind***: **{‘timestamp’, ‘period’}, optional, default None**

​		传递'timestamp'将结果索引转换为DateTimeIndex，或'period'将其转换为PeriodIndex。默认情况下，保留输入表示形式。

​	***on***：**str, optional**

​		对于 DataFrame，使用列而不是索引来重新取样。列必须类似于 datetime。

​	***level***：**str or int, optional**

​		用于重采样的多索引、级别(名称或数字)。级别必须与日期时间类似。

​	***origin***：**{‘epoch’, ‘start’, ‘start_day’, ‘end’, ‘end_day’}, Timestamp**

​		调整分组的时间戳。原始时区必须与索引的时区匹配。如果不使用时间戳，也支持以下值:

​			1)"epoch":起源是1970年01月01日

​			2)"start": 起源是timeseries的第一个值

​			3)"start_day":起源是timeseries午夜的第一天

​			4)"end"：起源是TimeSeries的最后一个值

​			5)"end_day"：起源是最后一天的午夜

​	***offset***：**Timedelta or str, default is None**

​		加到原点的偏移时间。

##### 注意：

​	更多信息请参阅[user guide](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#resampling)

​	要了解有关偏移字符串的更多信息，请参阅 [this link](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#dateoffset-objects)

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.resample.html)

#### **==DataFrame.to_period==**(freq=None, axis=0, copy=True)

###### 将 DataFrame 从 DatetimeIndex 转换为 PeriodIndex。用期望的频率将 DataFrame 从 DatetimeIndex 转换为 PeriodIndex (如果没有通过，则从索引中推断)。

##### 参数设置：

​	***freq***：**str, default**

​		周期指数的频率

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要转换的轴(默认为索引)

​	***copy***：**bool, default True**

​		如果为 False，则不复制基础输入数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_period.html)

#### **==DataFrame.to_timestamp==**(freq=None, how='start', axis=0, copy=True)

###### 期初时间戳的 DatetimeIndex 的强制转换。

##### 参数设置：

​	***freq***：**str, default frequency of PeriodIndex**

​		期望频率

​	***how***：**{‘s’, ‘e’, ‘start’, ‘end’}**

​		将期间转换为时间戳的约定; 期间开始与结束。

​	***axis***：**{0 or ‘index’, 1 or ‘columns’}, default 0**

​		要转换的轴(默认为索引)。

​	***copy***：**bool, default True**

​		如果为 False，则不复制基础输入数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_timestamp.html)

#### **==DataFrame.tz_convert==**(tz, axis=0, level=None, copy=True)

###### 将 tz 感知轴转换为目标时区。

##### 参数设置：

​	**tz**：**str or tzinfo object**

​	**axis**：**the axis to convert**

​	**level**：**int, str, default None**

​		如果坐标轴是 MultiIndex，则转换特定级别。否则必须为 None。

​	**copy**：**bool, default True**

​		还要复制基础数据。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tz_convert.html)

#### **==DataFrame.tz_localize==**(tz, axis=0, level=None, copy=True, ambiguous='raise', nonexistent='raise')

###### 将 Series 或 DataFrame 的 tz-naive 索引本地化为目标时区。此操作将索引本地化Series.dt.tz_localize().

##### 参数设置：

​	***tz***：**str or tzinfo**

​	***axis***：**the axis to localize**

​	***level***：**int, str, default None**

​		如果坐标轴是 MultiIndex，则转换特定级别。否则必须为 None。

​	***copy***：**bool, default True**

​		还要复制基础数据。

​	***ambiguous***：**‘infer’, bool-ndarray, ‘NaT’, default ‘raise’**

​		当时钟由于 DST 向后移动时，可能会出现模糊的时间。例如，在中欧时间(UTC + 01)中，从 DST 03:00到非 DST 02:00,02:30:00的当地时间既发生在 UTC 00:30:00，也发生在 UTC 01:30:00。在这种情况下，模糊参数规定了应该如何处理模糊时间。

​			‘infer’ 将尝试根据订单推断出DST-过渡时间

​			bool-ndarray 在其中TRUE表示DST时间，假指定非DST时间（请注意，此标志仅适用于模糊时间）

​			'NAT'将返回没有暧昧时间的NAT

​			如果存在暧昧时间，‘raise’ 将培养一个ambiguoustimeerror。

​	***nonexistent***：**str, default ‘raise’**

​		在特定时区内不存在的时间不存在，其中时钟由于DST向前移动。有效值是：

​			'shift_forward'将转移到最近的现有时间的不存在的时间

​			'shift_backward'将向后移动到最近的现有时间

​			'NAT'将返回NAT，其中不存在时间

​			Timedelta对象将由Timedelta迁移不存在的时间

​			如果存在不存在的时间，则‘raise’将提高一个非声明。

#### [官网](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tz_localize.html)

