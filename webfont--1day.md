# 웹폰트 파헤치기

### Webfont?
> 웹폰트는 클라이언트 컴퓨터에 폰트가 없는 경우, 서버에서 폰트 파일을 내려받아 표현해주는 기술

### 브라우저 지원
|   |IE|Edge|Chrome|FireFox|Opera|iOS Safari|Android|Samsung<br>Internet|
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|EOT|6+|X|X|X|X|X|X|X|
|SVG|X|X|X|X|X|3.2+|X|X|
|TTF/OTF|9+|12+|4+|3.5+|10.1+|4.3+|2.2+|4+|
|WOFF|9+|12+|5+|3.6+|11.5+|5.1+|4.4+|4+|
|WOFF2|X|14+|36+|39+|23+|10.2+|5+|4+|
> SVG : Chrome(37이하), Android(3~4.4.4), Samsung Internet(4이하)등에서 하위버전 지원, 최신버전에선 지원하지 않음
> <br>[Android 버전 정보](https://upload.wikimedia.org/wikipedia/commons/e/ee/Android_historical_version_distribution_-_vector.svg) : 4.3(Jelly Bean), 4.4(Kitkat)
> <br>브라우저 버전 정보 : [크롬](https://namu.wiki/w/크롬(웹%20브라우저)#s-4.1) / [Firefox](https://namu.wiki/w/모질라%20파이어폭스/버전)

### CSS 선언
```css
/* 
  local(폰트 그룹명), 
  local(단일 폰트명), 
  url(폰트경로) format(폰트포멧) 
*/
@font-face {
  font-weight: 100;
  font-family: NotoSans;
  src:local("NotoSans"), local("NotoSans-Thin"), url(https://papachooong.github.io/snippets/font/noto/NotoSansKR-Thin.woff) format('woff');
  unicode-range: U+AC01, U+AC08;
}
@font-face {
  font-weight: normal;
  font-family: NotoSans;
  src:local("NotoSans"), local("NotoSans-Regular"), url(https://papachooong.github.io/snippets/font/noto/NotoSansKR-Regular.woff) format('woff');
  unicode-range: U+AC01, U+AC08;
}
```
> [유니코드 표](https://ko.wikipedia.org/wiki/%EC%9C%A0%EB%8B%88%EC%BD%94%EB%93%9C_0000~0FFF)
> <br>사용할 유니코드의 범위를 정하며, 유니코드 범위 내 사용하는 문자가 없으면 웹폰트를 다운로드 하지 않는다고 함
> <br>이런 속성값이 있는지 몰랐는데, 국내환경만 제작할땐 모르겠지만, 글로벌 서비스를 만들 예정이라면 유용하게 쓰일 속성값일듯