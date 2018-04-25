Pandoc Template for Report (cs-ex1)
===

このテンプレートを使えばPandocを使って大学に提出するための講義用レポートを手軽に作成することができます．

某情報化学実験1向け．

## 概要
レポートをMarkdownで書いた後にPandocを使ってLaTeX形式もしくはPDF形式に出力することができます．
このテンプレートを使うことで，大学の講義用レポート向けに以下の設定が可能です．

## 動作環境
- Pandoc
- pandoc-crossref
- LuaTeX

## 使い方
```shell
pandoc -F pandoc-crossref sample.md -o output.pdf --template=./../template.tex --latex-engine=lualatex -N --listings -M "crossrefYaml=./config/crossref_config.yaml"
```

```markdown
---
documentclass: ltjsarticle
title: ナントカ回路 基礎編
experiment:
  - date: 平成30年4月19日(木)
    submitdate: 平成30年4月24日(火)
    deadline: 平成30年4月26日(木)
    authorid: T160D000
    author: 群馬太郎
    group: Z
coauthor:
  id: T160D999
  name: 高崎太郎
coauthor-sub:
  - id: T160D990
  	name: 渋川太郎
  - id: T1500000
  	name: ここは無限人増やせる
---
## 以下文章
これはサンプルテキストです
```

### ソースコードの張り付け
pandoc-crossrefによるソースコードの挿入ではなく，listingsを利用したソースコードの挿入を行う場合は以下のように挿入してください．
```markdown
'''{label=lst:helloworld .numberLines caption="サンプル" style=customc .listings}
#include <stdio.h>
int main(){
  printf("Hello, World!");
  return 0;
}
'''
```
labelを`lst:hogehoge`のように指定することで，listings環境を利用しても`[@lst:hogehoge]`のように引用することができます．

## ライセンス
GPLv2
- template.tex
  - (C) 2006-2017 John MacFarlane (jgm@berkeley.edu)
