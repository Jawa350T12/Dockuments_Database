
## Описание таблиц datasets
|Schema|Name|Type|Owner|
|------|----|----|-----|
|public|[channels](#chanels)|foreing table|dataset_admin
|public|[channels_v]|view|dataset_admin
|public|[equipment](#equipment)|foreing table|dataset_admin
|public|[equipment_channels](#equipment_chanels)|foreing table|dataset_admin
|public|[equipment_channels_v]|view|dataset_admin
|public|[equipment_v]|view|dataset_admin
|public|[fft_1](#fft_1)|table|dataset_admin
|public|[groups](#groups)|foreing table|dataset_admin
|public|[groups_v]|view|dataset_admin
|public|[list_blov](#list_blov)|table|dataset_admin
|public|[mes121](#mes121)|table|dataset_admin
|public|[mes121_v]|view|postgres
|public|[mes122](#mes122)|table|dataset_admin
|public|[mes122_v]|view|postgres
|public|[mes141](#mes141)|table|dataset_admin
|public|[mes141_v]|view|postgres
|public|[mes142](#mes142)|table|dataset_admin
|public|[mes142_v]|view|postgres
|public|[mes151](#mes151)|table|dataset_admin
|public|[mes151_v]|view|postgres
|public|[mes152](#mes152)|table|dataset_admin
|public|[mes152_v]|view|postgres
|public|[test_df](#test_df)|table|dataset_admin
|public|[trend_df](#trend_df)|table|dataset_admin

channels - <описание таблицы>
...

## Структура

![img](ERD_datasets.png)

## Таблицы

### chanels
|Column|Type|
|:-|:-:|
|channel_id|integer|
|channel_name|character varying(50)|
|channel_units|character varying(50)|
|channel_description|character varying(250)|
|memo|text|

channel_id - <какое-то описание>
channel_name -
channel_units -
channel_description -
memo - 

### equipment
|Column|Type|
|:-|:-:|
|equipment_id|integer|
|group_id|integer|
|equipment_name|character varying(200)|
|equipment_status|integer|
|plan_val|double precision|
|mac_address|character varying(50)|
|use_align_filter|boolean|
|align_filter_secs|bigint|
|std_window_secs|bigint|
|sort_order|integer|
|created|timestamp without time zone|

equipment_id - 
group_id -
equipment_name -
equipment_status -
plan_val -
mac_address -
use_align_filter -
align_filter_secs -
std_window_secs -
sort_order -
created -

### equipment_chanels
|Column|Type|
|:-|:-:|
|id|bigint|
|equipment_id|integer|
|channel_id|integer|
|sens_level|double precision|
|is_active|boolean|
|mac_address|character varying(50)|
|channel_alias|character varying|
|use_std|boolean|
|std_level|real|
|szero|double precision|
|koef|double precision|

id -
equipment_id -
channel_id -
sens_level -
is_active -
mac_address-
channel_alias -
use_std -
std_level -
szero -
koef -

### fft_1
|Column|Type|
|:-|:-:|
|eqt|bigint|
|channel|bigint|
|moment|timestamp without time zone|
|Y|bigint|
|X|bigint|
|val|bigint|

### groups
|Column|Type|
|:-|:-:|
|group_id|integer|
|parent_id|integer|
|group_name|character varying(200)|
|group_status|integer|

### list_blov
|Column|Type|
|:-|:-:|
|id|integer|
|number|integer|
|name|character varying(100)
|describe|text|
|equipment_id|integer|
|sensor|integer|
|channel_id|integer|
|cod|character(5)|

### mes121
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp whithout time zone
|tm|double precision|
|dlt|double precision|
|key|text|
|xyz|text|
|MAC|text|
|sensor|bigint|
|dt|text|

### mes122
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp whithout time zone
|tm|double precision|
|dlt|double precision|
|key|text|
|xyz|text|
|MAC|text|
|sensor|bigint|
|dt|text|

### mes141
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp without time zone|
|key|text|
|tm|double precision|
|hist|text|
|dlt|double precision|
|MAC|text|
|sensor|bigint|
|dt|text|
|mes_0|double precision|
|mes_1|double precision|
|mes_2|double precision|
|mes_3|double precision|
|mes_4|double precision|

### mes142
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp without time zone|
|key|text|
|tm|double precision|
|hist|text|
|dlt|double precision|
|MAC|text|
|sensor|bigint|
|dt|text|
|mes_0|double precision|
|mes_1|double precision|
|mes_2|double precision|
|mes_3|double precision|
|mes_4|double precision|


### mes151
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp without time zone|
|tm|double precision|
|dlt|double precision|
|key|text|
|MAC|text|
|sensor|bigint|
|dt|text|
|es_0|double precision|
|es_1|double precision|
|es_2|double precision|
|es_3|double precision|
|es_4|double precision|
|es_5|double precision|
|mes_6|double precision|
|mes_7|double precision|
|mes_8|double precision|
|mes_9|double precision|
|mes_10|double precision|

### mes152
|Column|Type|
|:-|:-:|
|mac_id|bigint|
|channel|bigint|
|moment|timestamp without time zone|
|tm|double precision|
|dlt|double precision|
|key|text|
|MAC|text|
|sensor|bigint|
|dt|text|
|es_0|double precision|
|es_1|double precision|
|es_2|double precision|
|es_3|double precision|
|es_4|double precision|
|es_5|double precision|
|mes_6|double precision|
|mes_7|double precision|
|mes_8|double precision|
|mes_9|double precision|
|mes_10|double precision|

### test_df
|Column|Type|
|:-|:-:|
|moment| without time zone|
|mean|double precision|
|min_|double precision|
|max_|double precision|
|std| double precision|
|kmax|double precision|
|kmin|double precision|
|peak_factor|double precision|

### trend_df
|Column|Type|
|:-|:-:|
|date|timestamp without time zone|
|max_mean|double precision|
|min_mean|double precision|
|mean_mean|double precision|
|std_mean|double precision|
|max_peak|double precision|
|min_peak|double precision|
|anomalies_count |bigint|
|peaks_count|bigint|
|kmax_avg|double precision|
|kmin_avg|double precision|
|max_peak_factor|double precision|
|min_peak_factor|double precision|
|mean_peak_factor|double precision|
|std_peak_factor|double precision|
|array_|text|