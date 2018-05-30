# AWK-Study

## 1. NF, 字段的数量

Awk 计算当前输入行的字段数量, 并将它存储在一个内建的变量中, 这个变量叫作 NF. 因此程序{ print NF, $1, $NF }
将会打印每一个输入行的字段数量, 第一个字段, 以及最后一个字段.
测试数据emp.data 
```
Beth 0
Dan 0
Kathy 10
Mark 20
Mary 22
Susie 18
```
cat emp.data 
```
[root@xen10-18 awk]# cat emp.data 
Beth 0
Dan 0
Kathy 10
Mark 20
Mary 22
Susie 18
[root@xen10-18 awk]# cat emp.data 
Beth 0
Dan 0
Kathy 10
Mark 20
Mary 22
Susie 18
```

## 2.BEGIN 与 END

```
[root@xen10-18 awk]# awk 'BEGIN {print "字段个数 名字 最后一列"} { print NF, $1, $NF } END {print "字段个数END 名字END 最后一列END"}' emp.data     
字段个数 名字 最后一列
2 Beth 0
2 Dan 0
2 Kathy 10
2 Mark 20
2 Mary 22
2 Susie 18
字段个数END 名字END 最后一列END
```

## 3.打印行号

awk '{ print NR, $0 }' emp.data 

```
[root@xen10-18 awk]# awk '{ print NR, $0 }' emp.data 
1 Beth 0
2 Dan 0
3 Kathy 10
4 Mark 20
5 Mary 22
6 Susie 18

```
