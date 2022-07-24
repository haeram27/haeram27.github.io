
Forked from  
[`https://mmistakes.github.io/minimal-mistakes/`](https://mmistakes.github.io/minimal-mistakes/)
[`https://choiis.github.io/`](https://choiis.github.io/)
  
  
  
---
## 🦥 `haeram27 Devlog`


📎 **블로그 바로 가기**
[`https://haeram27.github.io/`](https://haeram27.github.io/)

---

### fork 주의사항 ★
**아래 사항들을 꼭 변경해주셔야 설정된 analytics에 영향이 되지 않습니다!!!**  

1. \_config.yml 변경

```yml
google_site_verification: "직접 추가하시거나 삭제해주세요"
bing_site_verification:
yandex_site_verification:
naver_site_verification: "직접 추가하시거나 삭제해주세요"
```

```yml
# Analytics
analytics:
  provider: "google-gtag"
  # false (default), "google", "google-universal", "google-gtag", "custom"
  google:
    tracking_id: "직접 추가하시거나 삭제해주세요"
    anonymize_ip: # true, false (default)
```

2. 아래 4개 파일 삭제

- googl~~~.html
- feed.xml
- naverc~~~.html
- robots.txt

**Comment 설정**  

1. utterances 셋팅

- [utterances](https://github.com/apps/utterances) 접속
- repository 선택 후 install
- 이 Jekyll Theme에서는 셋팅 방법이 다름.
- Enable Utterances script를 기억

2. _config.yml 수정

```yml
# 1번의 script에서 issue_term과 theme을 아래와 같이 작성
# 1번의 script와 _config.yml이 다를 경우만 수정
comments:
  provider: "utterances"
  utterances: 
    theme: "github-light" # "github-dark"
    issue_term: "pathname" # pathname은 post.md 파일 이름으로 연결됨
```

3. 본인 github에 public repo 생성 (repo명 : blog-comments)

4. _includes/comments-providers/utterances.html 수정

```html
var script = document.createElement('script');
script.setAttribute('src', 'https://utteranc.es/client.js');
script.setAttribute('repo', '본인아이디/blog-comments'); # 3에서 만들었던 레포지토리로 수정
```

5. comment 기능은 issue를 tracking하는 것이기 때문에 issue 관련 permission이 있다면 허용

