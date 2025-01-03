---
title: 조회수(analytics) 기능 - goatcounter
description: 블로그에 누가, 얼마나 들어왔지 볼 수 있는 조회수 시스템 설정하는 법을 알려줍니다.
author: AIWAB
date: 2024-11-17 21:42:00 +0800
categories: [Blogging, Postings]
tags: [typography]
pin: true
math: true
mermaid: true
---

## 검색 노출

- 블로그가 만들어졌다면, 다른 사람들이 들어올 수 있어야 합니다. 다른 사람들이 검색으로 내 블로그를 찾아 들어올 수 없다면 블로그가 갖는 기능 대부분이 사라지는 것과 마찬가지입니다.
- 모든 내용은 `jekyll`의 `chirpy` 테마를 기준으로 합니다.

### Google search console[](http://127.0.0.1:4000/posts/search/#google-search-console)

1. [google search console](https://search.google.com/search-console/about)에 접속합니다.
    
2. 회원가입 또는 로그인 후 `Start now` 버튼을 눌러줍니다.
![Start Now](/assets/img/md_img/start_now.png)
    

3. `URL prefix`에 자신의 `github` 주소를 입력하고 `CONTINUE`를 눌러줍니다.
![Github 주로를 URL prefix에 입력하세요.](/assets/img/md_img/URL_prefix.png)

4. **다른 확인 방법**의 `HTML 태그` 부분을 눌러 메타태그의 `content="~~"`의 ~~ 부분을 복사하여 `_config.yml` 파일의 `webmaster_verifications:`에 붙여 넣습니다.
    ```
    # Site Verification Settings
    webmaster_verifications:   
    google: ~~   
    bing: # fill in your Bing verification code
    alexa: # fill in your Alexa verification code 
    yandex: # fill in your Yandex verification code
    baidu: # fill in your Baidu verification code
    facebook: # fill in your Facebook verification code  
    ```
    
5. 파일을 `commit`과 `push`를 해준 후 아래 확인 버튼을 누르면 소유권을 확인했다는 성공 화면이 나옵니다. 만약 되지 않는다면 다시 `commit`과 `push`를 하여 확인해보십시오.
    
6. `Indexing` 카테고리의 `Sitemaps`로 들어가서 `Add a new sitemap`에 `/sitemap.xml`을 작성하여 `SUBMIT`을 눌러주면 사이트맵이 제출됩니다.
![현재 오류 있음](/assets/img/md_img/could't_fetch.png)
- 하지만 현재 오류로 가져올 수 없다고 뜹니다. 시간이 지나면 성공 표시가 뜨면 완성됩니다.

### Naver search advisor

1. [naver search advisor](https://searchadvisor.naver.com/)에 접속하여 회원가입/로그인을 하고 이용약관에 동의한 후 아래로 스크롤 하여 `웹마스터 도구 사용하기`를 눌러줍니다.
![웹마스터 도구 사용하기](/assets/img/md_img/webmaster_tool.png)

2. 사이트 등록에 블로그 주소를 입력하여 등록해줍니다.
![블로그 주소 등록](/assets/img/md_img/site_submit.png)

3. `HTML 파일 업로드`를 누르고, `HTML 확인파일` 글씨를 눌러 HTML 파일을 [사용자].github.io 폴더 아래에 다운로드 한 후 소유확인을 눌러주면 사이트가 등록됩니다.
![HTML파일 업로드](/assets/img/md_img/html_file.png)

4. 자신의 블로그 주소를 눌러 들어간 후 `요청` - `사이트맵 제출`을 눌러준 후 `사이트맵 URL 입력` 공간에 [블로그 주소]/sitemap.xml (ex. https://shkang04.github.io/sitemap.xml)을 입력하고 `확인`버튼을 눌러줍니다.
![확인](/assets/img/md_img/naver_last.png)