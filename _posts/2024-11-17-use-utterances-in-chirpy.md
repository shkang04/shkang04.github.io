---
title: use-utterances-in-chirpy
description: 
author: shkang
date: 2024-11-17 17:55:00 +0800
categories: [Blogging, Demo]
tags: [typography]
pin: true
math: true
mermaid: true
---

# 댓글 기능
- 블로그에 댓글 기능을 추가하기 위해 github의 **utterances**를 사용합니다. **utterance**를 사용하는 이유는 광고가 없고, 가벼우며, github 계정 로그인을 통해 내 저장소의 issue에 댓글이 올라오는 시스템이기 때문에 유용하기 때문입니다.

1. 댓글 이슈가 올라올 저장소를 정한 후, [utterance](https://github.com/apps/utterances)에 접속하여 
   `Only Select Repository`를 통해 `댓글 issue`가 올라올 저장소를 선택하여 설치합니다.

2. `Repository`의 `repo:` 부분에 `댓글 issue`를 받을 저장소의 `permalink`를 입력 하고(ex. ksrina/karina.github.io), `Blog Post ↔️ Issue Mapping`부분은 `Issue title contains page pathname`을 선택한다.
   
3. `Enable Utterances`부분에 있는 코드를 복사하여 `post.html` 파일의 가장 아래에 붙여넣고, 
   `_config.yml` 파일의 `comments:` 부분을
``` title:"예시"
   utterances:
    repo: "shkang04/shkang04.github.io"
    issue_term: "pathname"
```
다음과 같이 작성해주면 완성됩니다.