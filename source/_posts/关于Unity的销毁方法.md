---
layout: port
title: 关于Unity物体的销毁方法
date: 2019-05-30 20:38:42
tags: Unity
---

>Destroy(异步销毁):
>
该函数并不是立即销毁物体而是给物体加了一个标识符，物体还在内存中，在下一帧时才销毁并从内存中移除。
>
DestroyImmediate:
>
立即销毁物体并移除内存。