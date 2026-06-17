# apex → www redirect

`infinit-c.com`(apex, 맨 도메인)을 `https://www.infinit-c.com`로 보내기 위한 GitHub Pages 사이트.

- 실제 홈페이지(www)는 **Cloudflare Pages**에서 서빙됨 (이 repo와 무관).
- 이 repo는 apex로 들어온 요청을 www로 **리다이렉트만** 한다.
- apex는 CNAME을 못 걸고 hosting.kr이 ALIAS/ANAME을 지원하지 않아, GitHub Pages의 고정 A IP + 무료 HTTPS를 이용한다.

## DNS (hosting.kr)
apex `@` A 레코드를 GitHub Pages IP로 설정:
```
@  A  185.199.108.153
@  A  185.199.109.153
@  A  185.199.110.153
@  A  185.199.111.153
```
`CNAME` 파일이 커스텀 도메인(`infinit-c.com`)을 지정한다.
