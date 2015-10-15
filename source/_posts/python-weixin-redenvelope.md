title: Python微信红包算法 python-weixin-redenvelope-algorithm
description: Python微信红包算法 python-weixin-redenvelope
date: 2015-02-15 18:05:51
updated: 2015-10-15 18:05:51
categories: python, algorithm
tags: [python, weixin, algorithm]
keywords: python, weixin, algorithm
---

Python微信红包算法

<!-- more -->


#### Python实现微信红包算法

```
# -*- coding: utf-8 -*-
import random
import sys

def randBonus(min, max, total,num):
    print min, max, total, num
    #print "{:.2f}".format(3.1415029)
    total = float(total)
    num = int(num)
    min = 0.01

    if num < 1:
        return
    if num == 1:
        print "第%d个人拿到红包数:%.2f" % (num,total)
        return
    i = 1
    totalMoney = total
    while(i < num):
        max = totalMoney - min*(num- i)
        k = int((num-i)/2)
        if num -i <= 2:
            k = num -i
        max = max/k
        monney = random.randint(int(min*100), int(max*100))
        monney = float(monney)/100
        totalMoney = totalMoney - monney
        print "第%d个人拿到红包为:%.2f, 余额:%.2f"%(i,monney,totalMoney)
        i += 1

    print "第%d个人拿到红包为:%.2f, 余额:%.2f"%(i,totalMoney,0.00)

if __name__ == '__main__':
    min = sys.argv[1]
    max = sys.argv[2]
    total = sys.argv[3]
    num = sys.argv[4]
    randBonus(min, max, total, num)
```



执行结果如下:

```
$ python bonus.py 0.01 10 20 10
0.01 10 20 10
第1个人拿到红包为:0.18, 余额:19.82
第2个人拿到红包为:2.05, 余额:17.77
第3个人拿到红包为:5.27, 余额:12.50
第4个人拿到红包为:0.90, 余额:11.60
第5个人拿到红包为:0.35, 余额:11.25
第6个人拿到红包为:1.77, 余额:9.48
第7个人拿到红包为:2.31, 余额:7.17
第8个人拿到红包为:0.75, 余额:6.42
第9个人拿到红包为:6.24, 余额:0.18
第10个人拿到红包为:0.18, 余额:0.00
```


