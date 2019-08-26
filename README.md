# HSR_version1
    高速铁路能力要素基础数据平台
    高速铁路能力要素管理信息系统使用说明书
一、高速铁路能力要素管理信息系统登录界面：
在vs2013中运行改程序，首先进入系统登陆界面，如图1-1所示。
![图1-1](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/21efaf9969553dcef75fbbbde1c9bcc.png)

图1-1高速铁路能力要素管理信息系统登陆界面

系统登陆架构需要输入用户名和密码进行登陆，其界面设计如图4-2所示，用户名和密码现阶段仅限指定用户登录，若输入错误，则无法登陆。
二、高速铁路能力要素管理信息系统主界面：
1. 高速铁路宏观网络可视化模块：
高速铁路宏观网络可视化界面体系侧重宏观网络展示，包括高速铁路网络可视化功能、高速铁路能力要素查询/修改功能、高铁票价查询与客流需求预测功能、高铁换乘客流统计功能、铁路票务信息管理功能。

高速铁路网络可视化功能中展示了全国投入运营的高铁线路：利用Html5和Echarts等可视化技术，爬取中国高铁主要节点，实现四纵四横高铁网络在网络中的显示和标记，在此基础上利用C#中Web Browser控件实现系统调取制作的网页信息和可视化，完成系统高速铁路宏观网络的展示；不同颜色表示不同的高铁线路，右下角包含对应线路的实例图标，单击对应的实例图标后，线路在界面上会突出显示。另外，用户可点按鼠标左键在界面中拖拽移动地图，鼠标指针悬浮时可查看地图中指向的车站和线路概况；鼠标左键单击对应车站可跳转至对应的车站地图可视化模块中。各模块通过Webbrowser控件及相关功能实现Html嵌入C#界面，利用Access数据库实现数据的传递，并通过一系列鼠标交互，可提供客流情况、票务信息、能力要素类型等粗略的页面信息，如图2-1所示：

![图2-1](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/0e0285d0cacab3768192e9634edbba7.png)

图2-1高速铁路宏观网络可视化界面

2. 高速铁路车站地图可视化模块：
高速铁路车站地图可视化界面体系侧重展现站场站台、股道、道岔布置等细节信息，同时提供车站图片信息，车站CAD展示，车站基本要素信息展示等。该地图可视化界面是利用Html5、JavaScript与Css等技术，结合OpenStreetMap地图技术实现的车站地图示意。在高速铁路网络线路示意图中，放大地图场景至13级，利用Mouseclick事件功能，鼠标左键单击该界面引用OpenStreetMap.org中相关接口，通过leaflet前端技术，利用PopUp、Mousemove等事件功能实现网页内部轻度交互功能。目前已经实现全国各省市、高速铁路车站、高铁线路区间的地图调取和股道展示，界面详情如图2-2所示：

 ![图2-2](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/77e9a55d1eb1fe418bcdd0eddbd33c3.png)
 
图2-2高速铁路车站地图可视化界面

三、高速铁路能力要素管理信息系统要素管理界面：
打开“数据管理”中的“能力要素”按钮（如图3-1所示）即可进入该界面。该模块将所有的能力要素均需接入数据库中，通过数据库sql接口与C# winform系统平台对接，多语言共同实现能力要素数据增删改查等功能。

 ![图3-1](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/a4ddec1e38bc74e07ef47d84d589894.png)
 
图3-1选择数据管理中能力要素管理选项

在该界面中首先选择“京沪高铁”线路，之后便可查阅京沪高铁的所有相关数据。查询操作和结果反馈如图3-2、3-3所示：

 ![图3-2](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/00e2690b031e48645f06d530b180cf9.png)
 
图3-2选择京沪高铁选项

 ![图3-3](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/8f3bbafffc36d86ca3e983d71ea392e.png)
 
图3-3能力要素浏览运行图要素

四、高速铁路能力要素管理信息系统运行图可视化界面：
点选“能力计算”菜单中的“运行图”选项即可进入能力统计分析模块，该模块可浏览京沪线路计划运行图及该线路对应的近几年跨线车比例变化图和客座率比例变化情况，如图4-1、4-2所示：

 ![图4-1](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/d48e2255b41d90f60d7f9cd250ee8dc.png)
 
 
图4-1选择能力计算中运行图选项

 ![图4-2](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/af1b124f8087dbf9174b2c2fc6a4957.png)
 
图4-2能力统计分析界面

该模块中利用ComponentOne图标控件与picture、datagridview图形和数据库控件实现能力统计值的分析和展示，如图4-2所示。左图区域可根据数据调整图像情况。右图区域中，右下区域为处理后可直接识别的运行图到发时刻数据，右上角部分为读取右下数据后利用C#GDI绘图技术，实现京沪高速铁路某日实绩运行图铺画。
五、高速铁路能力要素管理信息系统说明
针对高速铁路基础数据进行统一数据收集、处理、存储、查询和形象可视化展示等功能，系统基于.NET开发平台，采用C#语言开发高速铁路能力要素管理信息系统，并通过相应的案例对系统的进行展示。系统设计的目的在于在需求分析的基础上，设计出系统软件架构、数据结构以及各个功能模块，同时对系统中各功能进行详细设计，以此为基础来实现系统功能。
高速铁路能力要素管理信息系统的功能如下：
（1）	基础要素管理功能
对高速铁路通过能力要素信息进行存储和管理。高速铁路能力要素管理信息系统主要涉及到列车时刻表数据、列车径路信息、高速铁路路网信息（车站信息、城市信息、线路信息等）等能力计算相关基础数据。实现高速铁路网城市、车站、线路、区间、车站布置形式、列车运行控制方式、道岔型号等信息查询与管理，提供列车追踪间隔、区间限速等能力计算的各项作业时间标准，提供人机交互界面实现数据的查询、增加、修改、删除。系统能对上述的基础数据进行读取、格式校验和管理。
（2）	高速铁路宏观网络可视化功能
利用Html5和Echarts等可视化技术，爬取中国高铁主要节点，实现四纵四横高铁网络在网络中的显示和标记，在此基础上利用C#中Web Browser控件实现系统调取制作的网页信息和可视化，完成系统高速铁路宏观网络的展示。
（3）	高速铁路车站地图可视化功能
利用Html5和Openstreetmap等地图显示技术，筛选中国铁路网的图层信息。在此基础上捕捉17级瓦片信息，实现站场股道、站台、道岔布置等其他地图无法显示的可视化情况，实现部分要素在地图上的展示。
（4）	通过能力统计分析功能
通过对当日列车运行图数据进行爬取，系统平台中可以进行可视化展现，铺画列车运行图。同时针对某单一线路可分析断面车流量、跨线车占比情况、每段区间内车辆运行时间、徐蚌段等繁忙时间段统计，初步加工处理形成专业化指标，并进一步统计推演规律。以数字和图表等方式实现高铁线路能力计算结果的展示。
（5）	指标计算及图表分析功能
系统能对阐述的能力计算结果的评价指标进行计算，包括相关参数取值等。其次，系统能通过Echarts等技术、ComponentOne等C#控件以数字和图表等形式对相应的评价指标进行展示，以及能对多个能力计算方案的各项指标进行对比。最后，系统应该提供相应的人机交互界面使得用户可以按照自己的业务需求选择要分析以及展示的指标。根据列车运行图数据，实现线路通过能力利用分析，分析区间断面列车数量、跨线车比例、区间列车速差分析。
针对高速铁路基础设计平台需求分析，本文对系统平台的功能进行了设计，划分为前端应用和后台管理两大模块。系统前端应用模块包括高速铁路网络可视化，高铁车站地图查询，通过能力统计分析，指标计算与图表展示等四大功能模块系统后台管理模块包括基础要素管理储存，多维数据接口管理，用户权限管理等三大功能模块系统总体功能结构如图5-1所示。：

 ![图2-1](https://github.com/HighSpeedRailwayCapabilityElementSystem/HSR_version1/blob/master/d6b79a1e87f9c48d2a54dd77b833da8.png)
 
图5-1 系统总体功能结构图
