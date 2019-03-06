---
layout: post
title: Argparse模块
date: 2019-3-6
categories: blog
tags: [python]
description: 如题。
---

Python 命令行工具argparse模块使用详解


### 一、编码实例
<pre><code>
import argparse

def get_args():
    parse = argparse.ArgumentParser()
    parse.add_argument('-r',help='输入一个数字',type=int)
    parse.add_argument('-s',help='输入字符串',type=str)
    parse.add_argument('-a',help='输入地址',type=str)
    args = parse.parse_args()
    return args

def show(r,s,a):
    print(r)
    print(s)
    print(a)

if __name__ == '__main__':
    args = get_args()
    show(args.r,args.s,args.a)

</code></pre>

————————————————————————————————————————————————————————————————————
### 二、Terminal


<pre><code>
------->python text.py -h

usage: MonteCarlo.py [-h] [-r R] [-s S] [-a A]

optional arguments:
  -h, --help  show this help message and exit
  -r R        输入一个数字
  -s S        输入字符串
  -a A        输入地址

</code></pre>

-help or -h 很好的起到了提供帮助信息的作用。

<pre><code>
----->python MonteCarlo.py -r 55 -s ppp -a vsadfaq.csv

55
ppp
vsadfaq.csv


</code></pre>









