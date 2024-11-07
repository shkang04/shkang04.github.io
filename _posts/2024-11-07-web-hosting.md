---
title: Web-Hosting
description: 
author: shkang
date: 2024-11-07 16:51:00 +0800
categories: [Blogging, Demo]
tags: [typography]
pin: true
math: true
mermaid: true
---
## 웹 구동 하면서 겪은 문제들

- VScode에서 F1을 누른 후 git clone이 안되어서 github에서 주소를 복사해 터미널에서 직접 git clone 하였습니다.
- `jekyll new./` 가 되지 않아서 `jekyll new./ --force` 로 강제 설치 하였습니다.
	- 그런데 설치가 비정상적으로 오래걸려 창을 껐다 켰더니 다시 정상적으로 설치가 되었습니다.
- github - Setting - Pages에서 Visit site를 눌렀을 때 화면에 이 문구만 떠서 `--- layout: home # Index page ---` 해결 방법을 찾아봤습니다. 해결 방법은 여러가지 있었으나 저는 `jekyll.yml`파일을 commit하면 고쳐진다는 방법이 있어서 이 방법을 통해 해결하였습니다.