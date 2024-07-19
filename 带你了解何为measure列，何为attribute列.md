---
title: "带你了解何为MEASURE列，何为ATTRIBUTE列"
date: "2019-03-12"
categories: 
  - "07"
  - "03"
  - "06"
---

DataFocus，是一款强大的数据可视化工具，要想将工具很好地用起来，那必须要了解DataFocus这个系统的设置。在DataFocus中，对于数据表中的列类型，只有两种，一种是MEASURE列，一种是ATTRIBUTE列，那到底什么是MEASURE列，什么是ATTRIBUTE列呢？下面主要把我对于这两种类型的理解分享给大家。

![](images/word-image-79.png)

MEASURE列：MEASURE，计量、测量。由此也可以推测出，MEASURE列主要是用来计算的，因此，MEASURE列必须是数值列，即MEASURE列的列中值必须全部为数值，例如上图中的销售金额、销售价格、销售数量等，在可视化中，相当于是图形展示的内容。那反过来，如果列中值全部为数值的，是不是就是MAESURE列？答案是不一定，原因在下面会讲到。

ATTRIBUTE列：ATTRIBUTE，属性。通常我们所知道的属性一般有，比如员工的个人信息：籍贯、性别、名称、地址等等。那由此我们推测出，ATTRIBUTE列就是属性信息，主要是文本信息，为什么说主要是文本信息？因为也有例外，比如，员工的手机号码，一般都是数值，但电话号码属于属性信息。ATTRIBUTE列在可视化中，相当于是图形展示需要的坐标轴，或者框架。

在数据表导入DataFocus时，系统怎么判断这一列是MEASURE列还是ATTRIBUTE列的呢？其实列类型，与导入系统的字段类型有关，若字段类型是timestamp（日期时间格式）、string（字符串格式）、boolean（布尔值格式），则系统会将该列识别成ATTRIBUTE列，若字段类型是int、double、bigint、smallint，则系统会将该列识别成MEASURE列。

![](images/word-image-80.png)

那有人会问了，两者之间可以互相转换吗？一般情况，MEASURE列可以转换成ATTRIBUTE列，但是相反的，ATTRIBUTE列不可以转换成MEASURE列，除了字段类型为boolean的，若字段类型为boolean的，在导入系统时，系统会自动识别成ATTRIBUTE列，但是此处的ATTRIBUTE列也可以转换成MEASURE列。

![](images/word-image-81.png)

MEASURE列—>ATTRIBUTE列

![](images/word-image-82.png)

字段类型：boolean

现在大家对于什么是ATTRIBUTE列，什么是MEASURE列有一定的了解了吧。
