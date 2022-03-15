---
title: "05 Gym Env"
date: 2021-05-04T22:09:39+09:00
draft: true
categories:
tags:
keywords:
---

# OpenAI/gymに倣ったEnvの作り方

## Basics

[gymのEnv](https://github.com/openai/gym)はunified environment interfaceであるため、Agents のための関数は定義されていない。Agentsとの接合部分の関数は自ら定義する必要がある。

次の関数は特に知っておくべき関数

- reset(self): 環境のStateをリセットする。（これを読む前の疑問としてEnvとStateの分離はどうやるのかわからなかったが、「環境の」Stateなので一体あるいは含まれているのかも）
- step(self, action): 1タイムステップだけ、環境を動かす。observation, reward, doneを返す。
- render(self, mode='human'): 環境の1フレームを描画する。デフォルトではユーザーフレンドリーな方法にすること推奨（GUIウィンドウなど）

