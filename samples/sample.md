---
documentclass: ltjsarticle
title: ナントカ回路 基礎編
experiment:
  - date: 平成30年4月19日(木)
    submitdate: 平成30年4月24日(火)
    deadline: 平成30年4月26日(木)
    authorid: T160D000
    author: 群馬太郎
    group: C
coauthor:
  id: T160D999
  name: 高崎太郎
coauthor-sub:
  - id: T160D990
  	name: 渋川太郎
---

# 概要
これは文章です．

プログラムは[@lst:helloworld]のように引用できます．

表は[@tbl:sample]のように書けます．

![図も挿入できます．[^fig]](sample.png){#fig:sample height=20mm}

[^fig]: 脚注です．

|a|b|
|-|-|
|1|2|
|3|4|

:表のサンプル {#tbl:sample}


$1 + 1 = 2$

# 付録
## プログラム1
``` {label=lst:helloworld .numberLines caption="Hello World" style=customc .listings}
#include <stdio.h>
int main(){
  printf("Hello, World!");
  return 0;
}
```
