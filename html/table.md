# table

## 表格属性

| **属性**    | **取值**                                                  | **描述**                              |
| ----------- | --------------------------------------------------------- | ------------------------------------- |
| align       | left、center、right                                       | 设置表格相对周围元素的对齐方式        |
| bgcolor     | rgb(x,x,x)、#xxxxxx、colorName                            | 设置表格的背景颜色                    |
| border      | 像素                                                      | 设置表格边框的宽度                    |
| cellpadding | 像素或百分比                                              | 设置单元格与其内容之间的距离          |
| cellspacing | 像素或百分比                                              | 设置单元格之间的距离                  |
| height      | 像素或百分比                                              | 设置表格的高度                        |
| width       | 像素或百分比                                              | 设置表格的宽度                        |
| rules       | none、groups、rows、cols、all                             | 设置表格中的表格线显示方式，默认是all |
| frame       | void、above、below、hsides、vsides、lhs、rhs、box、border | 设置表格的外部边框的显示方式          |

#### 对其方式
     align：left ，center ，right
#### 宽高   
     height："100";
     width: "250"
#### 背景颜色
     bgcolor :rgb() #xxxxxx ColorName
#### 边框
     border:1px;
#### 距离：
#####    单元格之间的距离  cellspacing
#####    单元格边框和内容之间的距离 cellpadding
#### 其他
     rules 表格线显示方式
     frame 表格的外部边框的显示方式   

## 行标签

| **属性**         | **描述**                                                  |
| ---------------- | --------------------------------------------------------- |
| align            | 设置单元格内容水平对齐方式：left、center、right、justify  |
| valign           | 设置单元格内容垂直对齐方式：top、middle、bottom、baseline |
| bgcolor          | 设置单元格的背景颜色                                      |
| bordercolor      | 设置行内单元格的边框颜色                                  |
| bordercolordark  | 设置行内单元格的右下边框颜色，IE支持                      |
| bordercolorlight | 设置行内单元格的左上边框颜色，IE支持                      |

## <thead> <tfoot> <tbody> <caption> 用于横向分组
**thead tfoot 只能出现一次** <++>

## 单元格属性

| **属性** | **描述**                                                    |
| -------- | ----------------------------------------------------------- |
| align    | 设置单元格内容的水平对齐方式：left、center、right、justify  |
| valign   | 设置单元格内容的垂直对齐方式：top、middle、bottom、baseline |
| rowspan  | 设置单元格跨越的行数                                        |
| colspan  | 设置单元格跨越的列数                                        |
| scope    | 定义将表头数据与单元数据相关联的方法                        |
| width    | 设置单元格的宽度                                            |
| height   | 设置单元格的高度                                            |
| bgcolor  | 设置单元格的背景颜色                                        |

**th标签一般用在表头 内容一般水平居中** 
**<th> <th> 中的空格浏览器不会显示，需要加&nbsp;以确保正常显示该单元格** 

## 