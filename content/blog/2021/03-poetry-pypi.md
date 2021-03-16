---
title: "Poetryで始める簡単パッケージ制作"
date: 2021-03-16T20:19:47+09:00
draft: false
categories:
- Python
tags:
- Python
- PyPI
- Poetry
keywords:
---

# Poetryで始める簡単パッケージ制作

## 準備

Poetryをインストール済みである

Poetryで管理された作業ディレクトリを構築している

## 手順

ビルドする

```terminal
poetry build
```

Configでテスト用PyPIのURLを指定する

```terminal
poetry config repositories.testpypi https://test.pypi.org/legacy/
```

公開する

この時、`--repository`オプションで先ほど指定したテスト用リポジトリを指定すればテスト用PyPIに公開できる

```terminal
poetry publish --repository testpypi
```

## まとめ

Poetryがなかった頃と比べて、ものすごく簡単だった。

ただし、PyPI向け`pyproject.toml`の整備はしてくれないので、別途指定する必要がある。

## 参照

- https://kk6.hateblo.jp/entry/2018/12/20/124151
- https://python-poetry.org/docs/cli/#publish