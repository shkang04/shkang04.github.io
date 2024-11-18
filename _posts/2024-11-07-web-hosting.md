---
title: Web-Hosting
description: 
author: AIWAB
date: 2024-11-07 16:51:00 +0800
categories: [Blogging, Demo]
tags: [typography]
pin: true
math: true
mermaid: true
---

## 웹 구동 하면서 겪은 문제들

1. VScode에서 F1을 누른 후 git clone이 안되어서 github에서 주소를 복사해 터미널에서 직접 git clone 하였습니다.

2. `jekyll new./` 가 되지 않아서 `jekyll new./ --force` 로 강제 설치 하였습니다.
	- 그런데 설치가 비정상적으로 오래걸려 창을 껐다 켰더니 다시 정상적으로 설치가 되었습니다.

3. github - Setting - Pages에서 Visit site를 눌렀을 때 화면에 이 문구만 떠서 `--- layout: home # Index page ---` 해결 방법을 찾아봤습니다. 해결 방법은 여러가지 있었으나 저는 `jekyll.yml`파일을 commit하면 고쳐진다는 방법이 있어서 이 방법을 통해 해결하였습니다.

4. 댓글 기능은 생각보다 쉽게 해결하였습니다. `_config.yml`파일의
``` title:"_config.yml"
utterances:
    repo: "shkang04/shkang04.github.io"
    issue_term: "pathname"
```
부분만 수정 후 `_layouts/post.html`파일의 맨 아래에
``` title:"_layouts/post.html"
<script src="https://utteranc.es/client.js"
        repo="shkang04/shkang04.github.io"
        issue-term="pathname"
        label="blog comment"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```
위 코드를 붙여 넣었습니다.

5. 조회수 기능은 (아직)정확히는 모르겠으나, goatcounter 사이트에서 visit이 증가하는 걸 볼 수 있었으나 제 웹사이트 내에서도 확인이 되어야 하는지 정확히 몰라서 visit이 증가하는 것만 확인 하였습니다. 제가 이 과정에서 겪은 문제점은 `_config.yml`파일의
``` title:"_config.yml"
analytics:
  google:
    id: # fill in your Google Analytics ID
  goatcounter:
    id: "https://aiwab.goatcounter.com/count"
```
위 부분에서 goatcounter의 id 끝에 `/count`를 붙이지 않아서 제대로 작동하지 않았었습니다.
또 `_includes/goatcounter.html`파일에 `<script data-goatcounter="https://aiwab.goatcounter.com/count" async src="//gc.zgo.at/count.js"></script>`를 붙여 넣어야 하는데 처음엔 어디에 이 코드를 붙여 넣어야 하는지 몰라서 작동되지 않았습니다.