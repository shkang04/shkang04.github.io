---
title: 조회수(analytics) 기능 - goatcounter
description: 
author: shkang
date: 2024-11-17 21:42:00 +0800
categories: [Blogging, Demo]
tags: [typography]
pin: true
math: true
mermaid: true
---

# 조회수 기능
- 내 웹 사이트에 사람들이 얼마나 들어왔는지 볼 수 있는 기능입니다. `구글 애널리틱스`와 `goatcounter` 등 많은 프로그램들이 있지만 `구글 애널리틱스`는 업데이트가 잦아 변동이 많을 수 있으므로 `goatcounter`를 사용할 것입니다.
- 모든 내용은 `jekyll`의 `chirpy` 테마를 기준으로 합니다.

1. [goatcounter.com](https://www.goatcounter.com/)에 접속하여 회원가입을 합니다.
   
2. 가입 시 입력한 메일로 인증을 마친 후 사이트에서 보여주는 코드를 복사하여 `goatcounter.html` 파일에 붙여 넣습니다.
   
3. `_config.yml` 파일의 `analytics:` 부분의 `goatcounter:`의 `id:`에 `https://[User_Code].goatcounter.com/count`를 작성해줍니다.