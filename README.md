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

## 2.BEGIN END

