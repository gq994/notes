# table标签

## 特性：

​     1.display:table,  特性类似于block，独占一行

​     2.表格的宽度默认是内容宽度，不会自动延伸

​     3.td或者th中，可以嵌套表格

​     4.表格每行的最大高度有该行最高的单元格决定

​     5.表格每列的最大宽度由该列最宽单元格决定

​     6.默认表格每列/行的宽/高度由表格宽/高度均分

​     7.tr和td或者th之间不能有其他任何标签

​     8.td或者th中可以放其他标签

##  表格的结构

```
 <table>                                   表格
          <caption></caption>              表格标题
          <colgroup>                       表格列组
            <col span="2" bgcolor="pink">  表示跨列两格，设置背景颜色
          </colgroup> 
          <thead></thead>                  表格头部
          <tbody>                          表格主体
            <tr>                           表格行
            <td>                           单元格/th为表头，也是一个单元格
              <td>
            </tr>
         </tbody>
         <tfoot></tfoot>                   表格脚部
</table>


```

##   align属性： 表格在父元素的空间下对齐

​       left   左对齐

​       center  居中

​       right  右对齐

##     border属性：边框

##     cellspacing属性：

表格单元格之间的间距，单元格往外产生间距

##     cellpadding属性：

单元格内填充，单元格往内产生间距

##     width属性：支持px、%百分比

##     height属性：支持px、%百分比

##     bgcolor属性：背景颜色

##  tr

###      align属性：当前行所有单元格内容对齐

​        left   左对齐

​        center  居中

​        right  右对齐

###      valign属性：

​        top   顶对齐

​        middle  居中对齐

​        bottom  底对齐

###      height属性：设置整行的高度

###      bgcolor属性：设置整行背景颜色