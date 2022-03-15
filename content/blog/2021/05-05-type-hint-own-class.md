---
title: "Type Hint Own Class"
date: 2021-05-05T19:33:15+09:00
draft: false
categories:
- Python
tags:
- Type annotation
keywords:
---

# Pythonで自身のクラスをクローンする関数の型ヒントの書き方

## Python version < 3.10

`from __future__ import annotations`を書くことで解決する。

## Python version >= 3.10

何もしなくても動く。

## References

- https://stackoverflow.com/questions/33533148/how-do-i-type-hint-a-method-with-the-type-of-the-enclosing-class