micaps文件 分部分 查看功能
2016     3    18         12     0     0   
年  月  日               时次  时效  层次（均为整数）


0.125     -0.125   60       150      60       -10   
经度格距  纬度格距  起始经度  终止经度  起始纬度  终止纬度（均为浮点数）

721        561   
纬向格点数  经向格点数（均为整数）  

2          -80          80      0       0
等值线间隔  等值线起始值  终止值  平滑系数 加粗线值（均为浮点数）



2016     3    18    12     0     0   

0.250  -0.250    60   150    60   -10   

361   281    

10     0   100     0    50




## 4
diamond  4  数据说明（字符串）  
	年  月  日  时次  时效  层次（均为整数）
	经度格距  纬度格距  起始经度  终止经度  起始纬度  终止纬度（均为浮点数） 
	纬向格点数  经向格点数（均为整数）  
	等值线间隔  等值线起始值  终止值  平滑系数 加粗线值（均为浮点数）

注：此类数据用于画格点数据的等值线。网格可以为经纬度网格，也可以为直角坐标网格。
1.当使用直角坐标网格数据时：
	1）将等值线终止值改为-1（直角坐标在兰勃托投影下）或-2（直角坐标在麦开托投影下）或-3（直角坐标在北半球投影下）。
	2）把网格经度间隔和纬度间隔改为格点数据第一行最后一个点的经纬度。
	3）把起始经度和起始纬度改为格点数据第一行第一个点的经纬度。
	4）把终止经度和终止纬度改为格点数据最后一行最后一个点的经纬度。
2.第4类数据文件可以直接用于填格点值。文件头中可以指定填图方式。指定方法为：
	1）把加粗线值改为-1，表示画等值线同时填图，
	2）改为-2表示只填图，不画等值线。

数据：
	数据按先纬向后经向放（直角坐标网格时为先X方向后Y方向），均为浮点数。
micaps4类数据存储的是格点数据。
其前两行的内容分别是“diamond 4 屏幕上需显示的内容”和“ 年 月 日 时次 时效 层次”。
第三行的信息是“经度格距 纬度格距 起始经度 终止经度 起始纬度 终止纬度 X-DIM Y-DIM 等值线间隔 等值线起始值 终止值 平滑系数 加粗线值”。
从第四行开始，就是格点数值了。这些数据的读取就是一个大的矩阵了。至于其中每个数值代表的地点，通过第三行的描述就能将其解析出来。

http://blog.csdn.net/HZGJF/article/details/4230109


## 14
diamond 14  数据说明（字符串）  年  月  日  时次 时效
- LINES
- LINES_SYMBOL
	表示槽线、冷锋等天气系统线条，其编码为：1—槽线、2—冷锋、3—暖锋、4—静止锋、5—锢囚锋、38—霜冻线、39—高温线。
- WithProp_LINESYMBOLS
	带属性线条数
- SYMBOLS
	编码 X  Y  Z  风向角度或字符串
- NOTES_SYMBOL
- CLOSED_CONTOURS
	闭合等值线
- WEATHER_REGION
	天气区的天气代码为：1—雨区、2—雪区、4—雷暴区、8—雾区、16—大风区、32—沙暴区。
	天气符号代码为：26-小雨、47-中雨、55-大雨、64-暴雨、25-阵雨、23-小雪、22-中雪、21-大雪、66-暴雪、65-阵雪、32-雷暴、31-冰雹、27-轻度雨凇、28-冻雨、24-雨夹雪、29-轻雾、30-雾、50-晴空、51-多云、52-阴天、42-龙卷、37-台风、44-霜冻、43-静风、40-34级风、36-45级风、33-56级风、41-67级风、34-78级风、35-89级风、101-910级风、102-1011级风、103-1112级风、60-高中心、61-低中心、62-暖中心、63-冷中心、48-文字注释
- FILLAREA







micaps
	按行分割
	去空行
	